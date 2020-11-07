---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7c766d3a112b880eaaa697e1f09d0d458dee5505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717806"
---
# <span data-ttu-id="63d8f-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="63d8f-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="63d8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="63d8f-103">Umożliwia zaktualizowanie opisu HybridConnection w określonej przestrzeni nazw przekazywania.</span><span class="sxs-lookup"><span data-stu-id="63d8f-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63d8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63d8f-104">SYNTAX</span></span>

### <span data-ttu-id="63d8f-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="63d8f-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63d8f-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="63d8f-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63d8f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63d8f-107">DESCRIPTION</span></span>
<span data-ttu-id="63d8f-108">Polecenie cmdlet Set-AzureRmRelayHybridConnection aktualizuje opis HybridConnection w określonej przestrzeni nazw Relay.</span><span class="sxs-lookup"><span data-stu-id="63d8f-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="63d8f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63d8f-109">EXAMPLES</span></span>

### <span data-ttu-id="63d8f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="63d8f-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid
```

### <span data-ttu-id="63d8f-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="63d8f-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"
```

<span data-ttu-id="63d8f-112">Umożliwia zaktualizowanie określonego HybridConnection przy użyciu nowego opisu w określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="63d8f-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="63d8f-113">W tym przykładzie zostanie zaktualizowana właściwość UserMetadata o nową wartość.</span><span class="sxs-lookup"><span data-stu-id="63d8f-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="63d8f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63d8f-114">PARAMETERS</span></span>

### <span data-ttu-id="63d8f-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="63d8f-115">-UserMetadata</span></span>
<span data-ttu-id="63d8f-116">Pobiera lub ustawia usermetadata jest symbolem zastępczym, aby można było przechowywać dane ciągu zdefiniowanego przez użytkownika dla punktu końcowego HybridConnection. na przykład można go użyć do przechowywania danych opisujących, takich jak lista zespołów i informacji kontaktowych, również w celu przechowywania ustawień konfiguracji zdefiniowanych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="63d8f-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="63d8f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63d8f-117">-Confirm</span></span>
<span data-ttu-id="63d8f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63d8f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63d8f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63d8f-119">-WhatIf</span></span>
<span data-ttu-id="63d8f-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63d8f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63d8f-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63d8f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63d8f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="63d8f-122">-InputObject</span></span>
<span data-ttu-id="63d8f-123">Obiekt HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="63d8f-123">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63d8f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63d8f-124">-Name</span></span>
<span data-ttu-id="63d8f-125">Nazwa HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="63d8f-125">HybridConnections Name.</span></span>

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

### <span data-ttu-id="63d8f-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="63d8f-126">-Namespace</span></span>
<span data-ttu-id="63d8f-127">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="63d8f-127">Namespace Name.</span></span>

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

### <span data-ttu-id="63d8f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d8f-128">-ResourceGroupName</span></span>
<span data-ttu-id="63d8f-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="63d8f-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="63d8f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d8f-130">-DefaultProfile</span></span>
<span data-ttu-id="63d8f-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63d8f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63d8f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d8f-132">CommonParameters</span></span>
<span data-ttu-id="63d8f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d8f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d8f-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63d8f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d8f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63d8f-135">INPUTS</span></span>

### <span data-ttu-id="63d8f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d8f-136">-ResourceGroupName</span></span>
<span data-ttu-id="63d8f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="63d8f-137">System.String</span></span>

### <span data-ttu-id="63d8f-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="63d8f-138">-NamespaceName</span></span>
<span data-ttu-id="63d8f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="63d8f-139">System.String</span></span>

### <span data-ttu-id="63d8f-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="63d8f-140">-WcfRelayName</span></span>
<span data-ttu-id="63d8f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="63d8f-141">System.String</span></span>

### <span data-ttu-id="63d8f-142">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="63d8f-142">-InputObject</span></span>
<span data-ttu-id="63d8f-143">Microsoft. Azure. Commands. Relay. modele. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="63d8f-143">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="63d8f-144">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="63d8f-144">-UserMetadata</span></span>
<span data-ttu-id="63d8f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="63d8f-145">System.String</span></span>

## <span data-ttu-id="63d8f-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63d8f-146">OUTPUTS</span></span>

### <span data-ttu-id="63d8f-147">Przykłady — 1: Inputobject</span><span class="sxs-lookup"><span data-stu-id="63d8f-147">Examples - 1 : InputObject</span></span>
<span data-ttu-id="63d8f-148">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:08:11 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: test UserMetadata identyfikator:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2 Name: TestHybirdConnection2 Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="63d8f-148">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:08:11 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="63d8f-149">Przykłady — 2: właściwości</span><span class="sxs-lookup"><span data-stu-id="63d8f-149">Examples - 2 : Properties</span></span>
<span data-ttu-id="63d8f-150">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:10:25 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: test UserMetadata zaktualizowany identyfikator:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1 Name: TestHybirdConnection1 Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="63d8f-150">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:10:25 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata updated Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="63d8f-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63d8f-151">NOTES</span></span>

## <span data-ttu-id="63d8f-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63d8f-152">RELATED LINKS</span></span>

