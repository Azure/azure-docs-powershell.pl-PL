---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 04022129d6709cf7dceea128b2813f97a5404234
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317773"
---
# <span data-ttu-id="afbae-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="afbae-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="afbae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afbae-102">SYNOPSIS</span></span>
<span data-ttu-id="afbae-103">Tworzy HybridConnection w określonym obszarze nazw przekaźnika.</span><span class="sxs-lookup"><span data-stu-id="afbae-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="afbae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afbae-104">SYNTAX</span></span>

### <span data-ttu-id="afbae-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="afbae-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afbae-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="afbae-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afbae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="afbae-107">DESCRIPTION</span></span>
<span data-ttu-id="afbae-108">Polecenie cmdlet New-AzRelayHybridConnection tworzy HybridConnection w określonym obszarze nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="afbae-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="afbae-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afbae-109">EXAMPLES</span></span>

### <span data-ttu-id="afbae-110">Przykład 1-Inputobject</span><span class="sxs-lookup"><span data-stu-id="afbae-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="afbae-111">Tworzy nowy HybirdConnection \` TestHybirdConnection2 \` w określonym obszarze nazw Relay \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="afbae-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="afbae-112">Przykład 2-Properties</span><span class="sxs-lookup"><span data-stu-id="afbae-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="afbae-113">Tworzy nowy HybirdConnection \` TestHybirdConnection1 \` w określonym obszarze nazw Relay \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="afbae-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="afbae-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afbae-114">PARAMETERS</span></span>

### <span data-ttu-id="afbae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afbae-115">-DefaultProfile</span></span>
<span data-ttu-id="afbae-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="afbae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afbae-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="afbae-117">-InputObject</span></span>
<span data-ttu-id="afbae-118">Obiekt HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="afbae-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afbae-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="afbae-119">-Name</span></span>
<span data-ttu-id="afbae-120">Nazwa HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="afbae-120">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afbae-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="afbae-121">-Namespace</span></span>
<span data-ttu-id="afbae-122">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="afbae-122">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afbae-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="afbae-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="afbae-124">prawda, jeśli autoryzacja klienta jest wymagana dla tego HybridConnections; w przeciwnym razie zwraca wartość FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="afbae-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="afbae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afbae-125">-ResourceGroupName</span></span>
<span data-ttu-id="afbae-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="afbae-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afbae-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="afbae-127">-UserMetadata</span></span>
<span data-ttu-id="afbae-128">Pobiera lub ustawia usermetadata jest symbolem zastępczym, aby można było przechowywać dane ciągu zdefiniowanego przez użytkownika dla punktu końcowego HybridConnection. na przykład można go użyć do przechowywania danych opisujących, takich jak lista zespołów i informacji kontaktowych, również w celu przechowywania ustawień konfiguracji zdefiniowanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="afbae-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="afbae-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="afbae-129">-Confirm</span></span>
<span data-ttu-id="afbae-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afbae-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afbae-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afbae-131">-WhatIf</span></span>
<span data-ttu-id="afbae-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afbae-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afbae-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="afbae-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afbae-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afbae-134">CommonParameters</span></span>
<span data-ttu-id="afbae-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afbae-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afbae-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afbae-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afbae-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afbae-137">INPUTS</span></span>

### <span data-ttu-id="afbae-138">System. String</span><span class="sxs-lookup"><span data-stu-id="afbae-138">System.String</span></span>

### <span data-ttu-id="afbae-139">Microsoft. Azure. Commands. Relay. modele. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="afbae-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="afbae-140">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="afbae-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="afbae-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afbae-141">OUTPUTS</span></span>

### <span data-ttu-id="afbae-142">Microsoft. Azure. Commands. Relay. modele. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="afbae-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="afbae-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afbae-143">NOTES</span></span>

## <span data-ttu-id="afbae-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afbae-144">RELATED LINKS</span></span>
