---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335854"
---
# <span data-ttu-id="e4cdc-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="e4cdc-101">New-AzRelayKey</span></span>

## <span data-ttu-id="e4cdc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="e4cdc-103">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="e4cdc-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="e4cdc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4cdc-104">SYNTAX</span></span>

### <span data-ttu-id="e4cdc-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e4cdc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4cdc-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e4cdc-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4cdc-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e4cdc-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4cdc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e4cdc-108">DESCRIPTION</span></span>
<span data-ttu-id="e4cdc-109">Polecenie cmdlet **New-AzRelayKey** generuje podstawowe i pomocnicze ciągi połączeń dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="e4cdc-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="e4cdc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4cdc-110">EXAMPLES</span></span>

### <span data-ttu-id="e4cdc-111">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="e4cdc-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e4cdc-112">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla podanej jednostki Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="e4cdc-113">Przykład 1,1 — dostarczona wartość podobszaru danych</span><span class="sxs-lookup"><span data-stu-id="e4cdc-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e4cdc-114">generuje podstawowy lub pomocniczy ciąg połączenia dla danej jednostki Relay-Namespace z podaną wartością klucza.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="e4cdc-115">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e4cdc-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e4cdc-116">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla podanej jednostki Relay-WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="e4cdc-117">Przykład 2,1-podano wartość WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e4cdc-118">generuje podstawowy lub pomocniczy ciąg połączenia dla danej jednostki Relay-WcfRelay z podaną wartością klucza.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="e4cdc-119">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e4cdc-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e4cdc-120">Generuje podstawowe lub pomocnicze parametry połączenia dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="e4cdc-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="e4cdc-121">Przykład 3,1-podano wartość HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e4cdc-122">generuje podstawowy lub pomocniczy ciąg połączenia dla danej jednostki Relay-HybridConnection z podaną wartością klucza.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="e4cdc-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4cdc-123">PARAMETERS</span></span>

### <span data-ttu-id="e4cdc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4cdc-124">-DefaultProfile</span></span>
<span data-ttu-id="e4cdc-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4cdc-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e4cdc-126">-HybridConnection</span></span>
<span data-ttu-id="e4cdc-127">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="e4cdc-128">-Wartość parametru</span><span class="sxs-lookup"><span data-stu-id="e4cdc-128">-KeyValue</span></span>
<span data-ttu-id="e4cdc-129">Zakodowany algorytm Base64 256-bitowy klucz do podpisywania i sprawdzania poprawności tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4cdc-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4cdc-130">-Name</span></span>
<span data-ttu-id="e4cdc-131">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e4cdc-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e4cdc-132">-Namespace</span></span>
<span data-ttu-id="e4cdc-133">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-133">Namespace Name.</span></span>

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

### <span data-ttu-id="e4cdc-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="e4cdc-134">-RegenerateKey</span></span>
<span data-ttu-id="e4cdc-135">Ponowne generowanie kluczy — "Primarykea"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="e4cdc-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="e4cdc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4cdc-136">-ResourceGroupName</span></span>
<span data-ttu-id="e4cdc-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4cdc-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e4cdc-138">-WcfRelay</span></span>
<span data-ttu-id="e4cdc-139">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="e4cdc-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4cdc-140">-Confirm</span></span>
<span data-ttu-id="e4cdc-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4cdc-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4cdc-142">-WhatIf</span></span>
<span data-ttu-id="e4cdc-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4cdc-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4cdc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4cdc-145">CommonParameters</span></span>
<span data-ttu-id="e4cdc-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4cdc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4cdc-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4cdc-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4cdc-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4cdc-148">INPUTS</span></span>

### <span data-ttu-id="e4cdc-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e4cdc-149">System.String</span></span>

## <span data-ttu-id="e4cdc-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4cdc-150">OUTPUTS</span></span>

### <span data-ttu-id="e4cdc-151">Microsoft. Azure. Commands. Relay. modele. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="e4cdc-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="e4cdc-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4cdc-152">NOTES</span></span>

## <span data-ttu-id="e4cdc-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4cdc-153">RELATED LINKS</span></span>
