---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 87682e5aa7b3c6ab5f7cc5ba4200d73f45960001
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240155"
---
# <span data-ttu-id="3e7d9-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="3e7d9-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="3e7d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e7d9-102">SYNOPSIS</span></span>
<span data-ttu-id="3e7d9-103">Pobiera podstawowe i pomocnicze ciągi połączeń dla danych obiektów przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3e7d9-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3e7d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3e7d9-104">SYNTAX</span></span>

### <span data-ttu-id="3e7d9-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3e7d9-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e7d9-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e7d9-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e7d9-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3e7d9-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e7d9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3e7d9-108">DESCRIPTION</span></span>
<span data-ttu-id="3e7d9-109">Polecenie **cmdlet Get-AzRelayKey** zwraca podstawowe i pomocnicze parametry połączenia dla danych obiektów przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3e7d9-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3e7d9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3e7d9-110">EXAMPLES</span></span>

### <span data-ttu-id="3e7d9-111">Przykład 1. Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="3e7d9-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="3e7d9-112">Przykład 2. WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3e7d9-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="3e7d9-113">Przykład 3. HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3e7d9-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="3e7d9-114">Podstawowe i pomocnicze ciągi połączenia do określonych obiektów przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="3e7d9-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="3e7d9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e7d9-115">PARAMETERS</span></span>

### <span data-ttu-id="3e7d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e7d9-116">-DefaultProfile</span></span>
<span data-ttu-id="3e7d9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e7d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e7d9-118">- HybridConnection</span><span class="sxs-lookup"><span data-stu-id="3e7d9-118">-HybridConnection</span></span>
<span data-ttu-id="3e7d9-119">Nazwa połączenia hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="3e7d9-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="3e7d9-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3e7d9-120">-Name</span></span>
<span data-ttu-id="3e7d9-121">Nazwa podmiotu autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3e7d9-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="3e7d9-122">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="3e7d9-122">-Namespace</span></span>
<span data-ttu-id="3e7d9-123">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="3e7d9-123">Namespace Name.</span></span>

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

### <span data-ttu-id="3e7d9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e7d9-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e7d9-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e7d9-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="3e7d9-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="3e7d9-126">-WcfRelay</span></span>
<span data-ttu-id="3e7d9-127">Nazwa aplikacji WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="3e7d9-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="3e7d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e7d9-128">CommonParameters</span></span>
<span data-ttu-id="3e7d9-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e7d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e7d9-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e7d9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e7d9-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e7d9-131">INPUTS</span></span>

### <span data-ttu-id="3e7d9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3e7d9-132">System.String</span></span>

## <span data-ttu-id="3e7d9-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e7d9-133">OUTPUTS</span></span>

### <span data-ttu-id="3e7d9-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="3e7d9-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="3e7d9-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3e7d9-135">NOTES</span></span>

## <span data-ttu-id="3e7d9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e7d9-136">RELATED LINKS</span></span>
