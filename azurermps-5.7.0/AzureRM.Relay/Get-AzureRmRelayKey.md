---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 897ecd66665091fd3be1f14b31c00549912a0af8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526621"
---
# <span data-ttu-id="24a1e-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="24a1e-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="24a1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="24a1e-103">Pobiera podstawowe i pomocnicze ciągi połączeń dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="24a1e-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24a1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24a1e-104">SYNTAX</span></span>

### <span data-ttu-id="24a1e-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24a1e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24a1e-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="24a1e-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24a1e-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="24a1e-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24a1e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="24a1e-108">DESCRIPTION</span></span>
<span data-ttu-id="24a1e-109">Polecenie cmdlet **Get-AzureRmRelayKey** zwraca podstawowe i pomocnicze parametry połączenia dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="24a1e-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="24a1e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24a1e-110">EXAMPLES</span></span>

### <span data-ttu-id="24a1e-111">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="24a1e-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### <span data-ttu-id="24a1e-112">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="24a1e-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### <span data-ttu-id="24a1e-113">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="24a1e-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="24a1e-114">Podstawowe i pomocnicze parametry połączenia z określonymi jednostkami przekazującymi (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="24a1e-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="24a1e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24a1e-115">PARAMETERS</span></span>

### <span data-ttu-id="24a1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a1e-116">-DefaultProfile</span></span>
<span data-ttu-id="24a1e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24a1e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24a1e-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="24a1e-118">-HybridConnection</span></span>
<span data-ttu-id="24a1e-119">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="24a1e-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="24a1e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24a1e-120">-Name</span></span>
<span data-ttu-id="24a1e-121">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="24a1e-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="24a1e-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="24a1e-122">-Namespace</span></span>
<span data-ttu-id="24a1e-123">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="24a1e-123">Namespace Name.</span></span>

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

### <span data-ttu-id="24a1e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a1e-124">-ResourceGroupName</span></span>
<span data-ttu-id="24a1e-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24a1e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="24a1e-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="24a1e-126">-WcfRelay</span></span>
<span data-ttu-id="24a1e-127">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="24a1e-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="24a1e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a1e-128">CommonParameters</span></span>
<span data-ttu-id="24a1e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24a1e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a1e-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a1e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a1e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24a1e-131">INPUTS</span></span>

### <span data-ttu-id="24a1e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a1e-132">-ResourceGroupName</span></span>
 <span data-ttu-id="24a1e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="24a1e-133">System.String</span></span> 

### <span data-ttu-id="24a1e-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="24a1e-134">-NamespaceName</span></span>
 <span data-ttu-id="24a1e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="24a1e-135">System.String</span></span> 
 

### <span data-ttu-id="24a1e-136">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="24a1e-136">-HybridConnectionsName</span></span>
 <span data-ttu-id="24a1e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="24a1e-137">System.String</span></span> 

### <span data-ttu-id="24a1e-138">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="24a1e-138">-WcfRelayName</span></span>
 <span data-ttu-id="24a1e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="24a1e-139">System.String</span></span> 

### <span data-ttu-id="24a1e-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24a1e-140">-Name</span></span>
 <span data-ttu-id="24a1e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="24a1e-141">System.String</span></span>

## <span data-ttu-id="24a1e-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24a1e-142">OUTPUTS</span></span>

### <span data-ttu-id="24a1e-143">Microsoft. Azure. Commands. Relay. modele. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="24a1e-143">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="24a1e-144">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="24a1e-144">Example 1 - Namespace</span></span>
<span data-ttu-id="24a1e-145">PrimaryConnectionString: punkt końcowy = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # deAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="24a1e-145">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="24a1e-146">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="24a1e-146">Example 2 - WcfRelay</span></span>
<span data-ttu-id="24a1e-147">PrimaryConnectionString: punkt końcowy = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # deAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="24a1e-147">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="24a1e-148">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="24a1e-148">Example 3 - HybridConnection</span></span>
<span data-ttu-id="24a1e-149">PrimaryConnectionString: punkt końcowy = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SecondaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # deAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="24a1e-149">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="24a1e-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24a1e-150">NOTES</span></span>

## <span data-ttu-id="24a1e-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24a1e-151">RELATED LINKS</span></span>

