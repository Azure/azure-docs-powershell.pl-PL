---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 050d6477a25922236dc2d9d2e28db1228f4666fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550587"
---
# <span data-ttu-id="5fad5-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="5fad5-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="5fad5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fad5-102">SYNOPSIS</span></span>
<span data-ttu-id="5fad5-103">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="5fad5-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fad5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fad5-104">SYNTAX</span></span>

### <span data-ttu-id="5fad5-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5fad5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fad5-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5fad5-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fad5-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5fad5-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fad5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5fad5-108">DESCRIPTION</span></span>
<span data-ttu-id="5fad5-109">Polecenie cmdlet **New-AzureRmRelayKey** generuje podstawowe i pomocnicze ciągi połączeń dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="5fad5-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="5fad5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fad5-110">EXAMPLES</span></span>

### <span data-ttu-id="5fad5-111">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="5fad5-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="5fad5-112">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="5fad5-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="5fad5-113">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="5fad5-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="5fad5-114">Generuje podstawowe lub pomocnicze parametry połączenia dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="5fad5-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="5fad5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fad5-115">PARAMETERS</span></span>

### <span data-ttu-id="5fad5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fad5-116">-DefaultProfile</span></span>
<span data-ttu-id="5fad5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fad5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fad5-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="5fad5-118">-HybridConnection</span></span>
<span data-ttu-id="5fad5-119">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="5fad5-119">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fad5-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5fad5-120">-Name</span></span>
<span data-ttu-id="5fad5-121">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="5fad5-121">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fad5-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5fad5-122">-Namespace</span></span>
<span data-ttu-id="5fad5-123">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="5fad5-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fad5-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="5fad5-124">-RegenerateKey</span></span>
<span data-ttu-id="5fad5-125">Ponowne generowanie kluczy — "Primarykea"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="5fad5-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fad5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fad5-126">-ResourceGroupName</span></span>
<span data-ttu-id="5fad5-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5fad5-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fad5-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="5fad5-128">-WcfRelay</span></span>
<span data-ttu-id="5fad5-129">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="5fad5-129">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fad5-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5fad5-130">-Confirm</span></span>
<span data-ttu-id="5fad5-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fad5-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fad5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fad5-132">-WhatIf</span></span>
<span data-ttu-id="5fad5-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fad5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fad5-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5fad5-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fad5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fad5-135">CommonParameters</span></span>
<span data-ttu-id="5fad5-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fad5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fad5-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fad5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fad5-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fad5-138">INPUTS</span></span>

### <span data-ttu-id="5fad5-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="5fad5-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="5fad5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5fad5-140">System.String</span></span> 

### <span data-ttu-id="5fad5-141">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5fad5-141">-NamespaceName</span></span>
 <span data-ttu-id="5fad5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5fad5-142">System.String</span></span> 
 

### <span data-ttu-id="5fad5-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="5fad5-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="5fad5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5fad5-144">System.String</span></span> 

### <span data-ttu-id="5fad5-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="5fad5-145">-WcfRelayName</span></span>
 <span data-ttu-id="5fad5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5fad5-146">System.String</span></span> 

### <span data-ttu-id="5fad5-147">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5fad5-147">-Name</span></span>
 <span data-ttu-id="5fad5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5fad5-148">System.String</span></span>

### <span data-ttu-id="5fad5-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="5fad5-149">-RegenerateKeys</span></span>
 <span data-ttu-id="5fad5-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5fad5-150">System.String</span></span>

## <span data-ttu-id="5fad5-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fad5-151">OUTPUTS</span></span>

### <span data-ttu-id="5fad5-152">Microsoft. Azure. Commands. Relay. modele. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="5fad5-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="5fad5-153">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="5fad5-153">Example 1 - Namespace</span></span>
<span data-ttu-id="5fad5-154">PrimaryConnectionString: punkt końcowy = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # deAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="5fad5-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="5fad5-155">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="5fad5-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="5fad5-156">PrimaryConnectionString: punkt końcowy = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # deAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="5fad5-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="5fad5-157">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="5fad5-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="5fad5-158">PrimaryConnectionString: punkt końcowy = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # deAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="5fad5-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="5fad5-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fad5-159">NOTES</span></span>

## <span data-ttu-id="5fad5-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fad5-160">RELATED LINKS</span></span>

