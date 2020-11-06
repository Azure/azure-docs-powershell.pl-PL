---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 7394ec382105b1d05bed589be95630f68ab79ae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550803"
---
# <span data-ttu-id="59565-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="59565-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="59565-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59565-102">SYNOPSIS</span></span>
<span data-ttu-id="59565-103">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="59565-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59565-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59565-104">SYNTAX</span></span>

### <span data-ttu-id="59565-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="59565-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59565-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="59565-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59565-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="59565-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59565-108">Opis</span><span class="sxs-lookup"><span data-stu-id="59565-108">DESCRIPTION</span></span>
<span data-ttu-id="59565-109">Polecenie cmdlet **New-AzureRmRelayKey** generuje podstawowe i pomocnicze ciągi połączeń dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="59565-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="59565-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59565-110">EXAMPLES</span></span>

### <span data-ttu-id="59565-111">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="59565-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="59565-112">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="59565-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="59565-113">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="59565-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="59565-114">Generuje podstawowe lub pomocnicze parametry połączenia dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="59565-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="59565-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59565-115">PARAMETERS</span></span>

### <span data-ttu-id="59565-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59565-116">-Confirm</span></span>
<span data-ttu-id="59565-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59565-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59565-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="59565-118">-HybridConnection</span></span>
<span data-ttu-id="59565-119">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="59565-119">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59565-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="59565-120">-Name</span></span>
<span data-ttu-id="59565-121">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="59565-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="59565-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="59565-122">-Namespace</span></span>
<span data-ttu-id="59565-123">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="59565-123">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59565-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="59565-124">-RegenerateKey</span></span>
<span data-ttu-id="59565-125">Ponowne generowanie kluczy — "Primarykea"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="59565-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59565-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59565-126">-ResourceGroupName</span></span>
<span data-ttu-id="59565-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="59565-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="59565-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="59565-128">-WcfRelay</span></span>
<span data-ttu-id="59565-129">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="59565-129">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59565-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59565-130">-WhatIf</span></span>
<span data-ttu-id="59565-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59565-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59565-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="59565-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59565-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59565-133">-DefaultProfile</span></span>
<span data-ttu-id="59565-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59565-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59565-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59565-135">CommonParameters</span></span>
<span data-ttu-id="59565-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59565-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59565-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59565-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59565-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59565-138">INPUTS</span></span>

### <span data-ttu-id="59565-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="59565-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="59565-140">System. String</span><span class="sxs-lookup"><span data-stu-id="59565-140">System.String</span></span> 

### <span data-ttu-id="59565-141">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="59565-141">-NamespaceName</span></span>
 <span data-ttu-id="59565-142">System. String</span><span class="sxs-lookup"><span data-stu-id="59565-142">System.String</span></span> 
 

### <span data-ttu-id="59565-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="59565-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="59565-144">System. String</span><span class="sxs-lookup"><span data-stu-id="59565-144">System.String</span></span> 

### <span data-ttu-id="59565-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="59565-145">-WcfRelayName</span></span>
 <span data-ttu-id="59565-146">System. String</span><span class="sxs-lookup"><span data-stu-id="59565-146">System.String</span></span> 

### <span data-ttu-id="59565-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="59565-147">-Name</span></span>
 <span data-ttu-id="59565-148">System. String</span><span class="sxs-lookup"><span data-stu-id="59565-148">System.String</span></span>

### <span data-ttu-id="59565-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="59565-149">-RegenerateKeys</span></span>
 <span data-ttu-id="59565-150">System. String</span><span class="sxs-lookup"><span data-stu-id="59565-150">System.String</span></span>

## <span data-ttu-id="59565-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59565-151">OUTPUTS</span></span>

### <span data-ttu-id="59565-152">Microsoft. Azure. Commands. Relay. modele. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="59565-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="59565-153">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="59565-153">Example 1 - Namespace</span></span>
<span data-ttu-id="59565-154">PrimaryConnectionString: punkt końcowy = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # deAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="59565-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="59565-155">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="59565-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="59565-156">PrimaryConnectionString: punkt końcowy = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # deAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="59565-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="59565-157">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="59565-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="59565-158">PrimaryConnectionString: punkt końcowy = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # deAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="59565-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="59565-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59565-159">NOTES</span></span>

## <span data-ttu-id="59565-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59565-160">RELATED LINKS</span></span>

