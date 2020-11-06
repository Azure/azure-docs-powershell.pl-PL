---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 315c50dbbc68865058f6c5663952fe2f42bc5c85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527325"
---
# <span data-ttu-id="214f2-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="214f2-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="214f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="214f2-102">SYNOPSIS</span></span>
<span data-ttu-id="214f2-103">Tworzy HybridConnection w określonym obszarze nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="214f2-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="214f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="214f2-104">SYNTAX</span></span>

### <span data-ttu-id="214f2-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="214f2-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="214f2-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="214f2-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="214f2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="214f2-107">DESCRIPTION</span></span>
<span data-ttu-id="214f2-108">Polecenie cmdlet New-AzureRmRelayHybridConnection tworzy HybridConnection w określonym obszarze nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="214f2-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="214f2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="214f2-109">EXAMPLES</span></span>

### <span data-ttu-id="214f2-110">Przykład 1-Inputobject</span><span class="sxs-lookup"><span data-stu-id="214f2-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection
```

<span data-ttu-id="214f2-111">Tworzy nowy HybirdConnection \` TestHybirdConnection2 \` w określonym obszarze nazw Relay \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="214f2-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="214f2-112">Przykład 2-Properties</span><span class="sxs-lookup"><span data-stu-id="214f2-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"
```

<span data-ttu-id="214f2-113">Tworzy nowy HybirdConnection \` TestHybirdConnection1 \` w określonym obszarze nazw Relay \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="214f2-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="214f2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="214f2-114">PARAMETERS</span></span>

### <span data-ttu-id="214f2-115">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="214f2-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="214f2-116">prawda, jeśli autoryzacja klienta jest wymagana dla tego HybridConnections; w przeciwnym razie zwraca wartość FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="214f2-116">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f2-117">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="214f2-117">-UserMetadata</span></span>
<span data-ttu-id="214f2-118">Pobiera lub ustawia usermetadata jest symbolem zastępczym, aby można było przechowywać dane ciągu zdefiniowanego przez użytkownika dla punktu końcowego HybridConnection. na przykład można go użyć do przechowywania danych opisujących, takich jak lista zespołów i informacji kontaktowych, również w celu przechowywania ustawień konfiguracji zdefiniowanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="214f2-118">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f2-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="214f2-119">-Confirm</span></span>
<span data-ttu-id="214f2-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214f2-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="214f2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214f2-121">-WhatIf</span></span>
<span data-ttu-id="214f2-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214f2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214f2-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="214f2-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="214f2-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="214f2-124">-InputObject</span></span>
<span data-ttu-id="214f2-125">Obiekt HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="214f2-125">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f2-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="214f2-126">-Name</span></span>
<span data-ttu-id="214f2-127">Nazwa HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="214f2-127">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f2-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="214f2-128">-Namespace</span></span>
<span data-ttu-id="214f2-129">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="214f2-129">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="214f2-130">-ResourceGroupName</span></span>
<span data-ttu-id="214f2-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="214f2-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214f2-132">-DefaultProfile</span></span>
<span data-ttu-id="214f2-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="214f2-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="214f2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214f2-134">CommonParameters</span></span>
<span data-ttu-id="214f2-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214f2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214f2-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="214f2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214f2-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="214f2-137">INPUTS</span></span>

### <span data-ttu-id="214f2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="214f2-138">-ResourceGroupName</span></span>
<span data-ttu-id="214f2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="214f2-139">System.String</span></span>

### <span data-ttu-id="214f2-140">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="214f2-140">-NamespaceName</span></span>
<span data-ttu-id="214f2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="214f2-141">System.String</span></span>

### <span data-ttu-id="214f2-142">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="214f2-142">-HybridConnectionsName</span></span>
<span data-ttu-id="214f2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="214f2-143">System.String</span></span>

### <span data-ttu-id="214f2-144">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="214f2-144">-InputObject</span></span>
<span data-ttu-id="214f2-145">Microsoft. Azure. Commands. Relay. modele. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="214f2-145">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="214f2-146">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="214f2-146">-RequiresClientAuthorization</span></span>
<span data-ttu-id="214f2-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="214f2-147">System.Boolean</span></span>

### <span data-ttu-id="214f2-148">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="214f2-148">-UserMetadata</span></span>
<span data-ttu-id="214f2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="214f2-149">System.String</span></span>

## <span data-ttu-id="214f2-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="214f2-150">OUTPUTS</span></span>

### <span data-ttu-id="214f2-151">Microsoft. Azure. Commands. Relay. modele. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="214f2-151">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="214f2-152">Przykłady — 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="214f2-152">Examples - 1 : InputObject</span></span>
<span data-ttu-id="214f2-153">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: RequiresClientAuthorization: prawda UserMetadata: Identyfikator meta danych użytkownika:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2 Name: TestHybirdConnection2 Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="214f2-153">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="214f2-154">Przykłady — 2: właściwości</span><span class="sxs-lookup"><span data-stu-id="214f2-154">Examples - 2 : Properties</span></span>
<span data-ttu-id="214f2-155">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: RequiresClientAuthorization: prawda UserMetadata: Identyfikator meta danych użytkownika:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1 Name: TestHybirdConnection1 Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="214f2-155">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="214f2-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="214f2-156">NOTES</span></span>

## <span data-ttu-id="214f2-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="214f2-157">RELATED LINKS</span></span>

