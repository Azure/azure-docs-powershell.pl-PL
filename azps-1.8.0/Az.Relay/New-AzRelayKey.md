---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: b768b7838629ce25e4202ca309de8741cfa7f0de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708471"
---
# <span data-ttu-id="dc46d-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="dc46d-101">New-AzRelayKey</span></span>

## <span data-ttu-id="dc46d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc46d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc46d-103">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dc46d-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="dc46d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc46d-104">SYNTAX</span></span>

### <span data-ttu-id="dc46d-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dc46d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc46d-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc46d-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc46d-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc46d-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc46d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dc46d-108">DESCRIPTION</span></span>
<span data-ttu-id="dc46d-109">Polecenie cmdlet **New-AzRelayKey** generuje podstawowe i pomocnicze ciągi połączeń dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dc46d-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="dc46d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc46d-110">EXAMPLES</span></span>

### <span data-ttu-id="dc46d-111">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="dc46d-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="dc46d-112">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla podanej jednostki Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="dc46d-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="dc46d-113">Przykład 1,1 — dostarczona wartość podobszaru danych</span><span class="sxs-lookup"><span data-stu-id="dc46d-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="dc46d-114">generuje podstawowy lub pomocniczy ciąg połączenia dla danej jednostki Relay-Namespace z podaną wartością klucza.</span><span class="sxs-lookup"><span data-stu-id="dc46d-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="dc46d-115">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dc46d-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="dc46d-116">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla podanej jednostki Relay-WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="dc46d-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="dc46d-117">Przykład 2,1-podano wartość WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="dc46d-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="dc46d-118">generuje podstawowy lub pomocniczy ciąg połączenia dla danej jednostki Relay-WcfRelay z podaną wartością klucza.</span><span class="sxs-lookup"><span data-stu-id="dc46d-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="dc46d-119">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dc46d-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="dc46d-120">Generuje podstawowe lub pomocnicze parametry połączenia dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dc46d-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="dc46d-121">Przykład 3,1-podano wartość HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="dc46d-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="dc46d-122">generuje podstawowy lub pomocniczy ciąg połączenia dla danej jednostki Relay-HybridConnection z podaną wartością klucza.</span><span class="sxs-lookup"><span data-stu-id="dc46d-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="dc46d-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc46d-123">PARAMETERS</span></span>

### <span data-ttu-id="dc46d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc46d-124">-DefaultProfile</span></span>
<span data-ttu-id="dc46d-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc46d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc46d-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dc46d-126">-HybridConnection</span></span>
<span data-ttu-id="dc46d-127">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="dc46d-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="dc46d-128">-Wartość parametru</span><span class="sxs-lookup"><span data-stu-id="dc46d-128">-KeyValue</span></span>
<span data-ttu-id="dc46d-129">Zakodowany algorytm Base64 256-bitowy klucz do podpisywania i sprawdzania poprawności tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="dc46d-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="dc46d-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc46d-130">-Name</span></span>
<span data-ttu-id="dc46d-131">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="dc46d-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="dc46d-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dc46d-132">-Namespace</span></span>
<span data-ttu-id="dc46d-133">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="dc46d-133">Namespace Name.</span></span>

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

### <span data-ttu-id="dc46d-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="dc46d-134">-RegenerateKey</span></span>
<span data-ttu-id="dc46d-135">Ponowne generowanie kluczy — "Primarykea"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="dc46d-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="dc46d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc46d-136">-ResourceGroupName</span></span>
<span data-ttu-id="dc46d-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc46d-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc46d-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dc46d-138">-WcfRelay</span></span>
<span data-ttu-id="dc46d-139">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="dc46d-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="dc46d-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc46d-140">-Confirm</span></span>
<span data-ttu-id="dc46d-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc46d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc46d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc46d-142">-WhatIf</span></span>
<span data-ttu-id="dc46d-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc46d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc46d-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dc46d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc46d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc46d-145">CommonParameters</span></span>
<span data-ttu-id="dc46d-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc46d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc46d-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc46d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc46d-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc46d-148">INPUTS</span></span>

### <span data-ttu-id="dc46d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="dc46d-149">System.String</span></span>

## <span data-ttu-id="dc46d-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc46d-150">OUTPUTS</span></span>

### <span data-ttu-id="dc46d-151">Microsoft. Azure. Commands. Relay. modele. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="dc46d-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="dc46d-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc46d-152">NOTES</span></span>

## <span data-ttu-id="dc46d-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc46d-153">RELATED LINKS</span></span>