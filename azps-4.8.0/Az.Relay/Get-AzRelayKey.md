---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 87682e5aa7b3c6ab5f7cc5ba4200d73f45960001
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220411"
---
# <span data-ttu-id="b0845-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="b0845-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="b0845-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0845-102">SYNOPSIS</span></span>
<span data-ttu-id="b0845-103">Pobiera podstawowe i pomocnicze ciągi połączeń dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b0845-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b0845-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0845-104">SYNTAX</span></span>

### <span data-ttu-id="b0845-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b0845-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0845-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b0845-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0845-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b0845-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0845-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b0845-108">DESCRIPTION</span></span>
<span data-ttu-id="b0845-109">Polecenie cmdlet **Get-AzRelayKey** zwraca podstawowe i pomocnicze parametry połączenia dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b0845-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b0845-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0845-110">EXAMPLES</span></span>

### <span data-ttu-id="b0845-111">Przykład 1: przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="b0845-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="b0845-112">Przykład 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b0845-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="b0845-113">Przykład 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b0845-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="b0845-114">Podstawowe i pomocnicze parametry połączenia z określonymi jednostkami przekazującymi (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="b0845-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b0845-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0845-115">PARAMETERS</span></span>

### <span data-ttu-id="b0845-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0845-116">-DefaultProfile</span></span>
<span data-ttu-id="b0845-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0845-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0845-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b0845-118">-HybridConnection</span></span>
<span data-ttu-id="b0845-119">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="b0845-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="b0845-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b0845-120">-Name</span></span>
<span data-ttu-id="b0845-121">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="b0845-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b0845-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b0845-122">-Namespace</span></span>
<span data-ttu-id="b0845-123">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="b0845-123">Namespace Name.</span></span>

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

### <span data-ttu-id="b0845-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0845-124">-ResourceGroupName</span></span>
<span data-ttu-id="b0845-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0845-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b0845-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b0845-126">-WcfRelay</span></span>
<span data-ttu-id="b0845-127">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="b0845-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="b0845-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0845-128">CommonParameters</span></span>
<span data-ttu-id="b0845-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0845-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0845-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0845-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0845-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0845-131">INPUTS</span></span>

### <span data-ttu-id="b0845-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b0845-132">System.String</span></span>

## <span data-ttu-id="b0845-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0845-133">OUTPUTS</span></span>

### <span data-ttu-id="b0845-134">Microsoft. Azure. Commands. Relay. modele. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b0845-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="b0845-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0845-135">NOTES</span></span>

## <span data-ttu-id="b0845-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0845-136">RELATED LINKS</span></span>
