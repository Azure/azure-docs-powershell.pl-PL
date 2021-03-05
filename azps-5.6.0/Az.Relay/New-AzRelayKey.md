---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: 078f8ec492e5cda6aea5c059f3b8493197ad358c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000522"
---
# <span data-ttu-id="ea4a3-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="ea4a3-101">New-AzRelayKey</span></span>

## <span data-ttu-id="ea4a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ea4a3-103">Ponowne generowanie podstawowych lub pomocniczych ciągów połączenia dla danego obiektów przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="ea4a3-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="ea4a3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ea4a3-104">SYNTAX</span></span>

### <span data-ttu-id="ea4a3-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ea4a3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea4a3-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea4a3-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea4a3-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea4a3-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea4a3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ea4a3-108">DESCRIPTION</span></span>
<span data-ttu-id="ea4a3-109">Polecenie **cmdlet New-AzRelayKey** generuje podstawowe i pomocnicze parametry połączenia dla danych obiektów przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ea4a3-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ea4a3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ea4a3-110">EXAMPLES</span></span>

### <span data-ttu-id="ea4a3-111">Przykład 1. Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="ea4a3-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ea4a3-112">Ponowne generowanie podstawowych lub pomocniczych ciągów połączenia dla danej Relay-Namespace encji.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="ea4a3-113">Przykład 1.1 . Podany klucz przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="ea4a3-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ea4a3-114">generuje podstawowe lub pomocnicze parametry połączenia dla danej jednostki Relay-Namespace z podaną wartością klucza</span><span class="sxs-lookup"><span data-stu-id="ea4a3-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="ea4a3-115">Przykład 2. WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ea4a3-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ea4a3-116">Ponowne generowanie podstawowych lub pomocniczych ciągów połączenia dla danej Relay-WcfRelay encji.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="ea4a3-117">Przykład 2.1 — WcfRelay KeyValue Provided</span><span class="sxs-lookup"><span data-stu-id="ea4a3-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ea4a3-118">generuje podstawowe lub pomocnicze parametry połączenia dla danej jednostki Relay-WcfRelay z podaną wartością klucza</span><span class="sxs-lookup"><span data-stu-id="ea4a3-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="ea4a3-119">Przykład 3. HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ea4a3-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ea4a3-120">Ponowne generowanie podstawowych lub pomocniczych ciągów połączenia dla encji przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ea4a3-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="ea4a3-121">Przykład 3.1 . HybridConnection KeyValue Provided</span><span class="sxs-lookup"><span data-stu-id="ea4a3-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="ea4a3-122">generuje podstawowe lub pomocnicze parametry połączenia dla danej jednostki Relay-HybridConnection z podaną wartością klucza</span><span class="sxs-lookup"><span data-stu-id="ea4a3-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="ea4a3-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea4a3-123">PARAMETERS</span></span>

### <span data-ttu-id="ea4a3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea4a3-124">-DefaultProfile</span></span>
<span data-ttu-id="ea4a3-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea4a3-126">- HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ea4a3-126">-HybridConnection</span></span>
<span data-ttu-id="ea4a3-127">Nazwa połączenia hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="ea4a3-128">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="ea4a3-128">-KeyValue</span></span>
<span data-ttu-id="ea4a3-129">Zakodowany w bazie danych klucz 256-bitowy do podpisywania i sprawdzania poprawności tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="ea4a3-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ea4a3-130">-Name</span></span>
<span data-ttu-id="ea4a3-131">Nazwa podmiotu autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="ea4a3-132">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="ea4a3-132">-Namespace</span></span>
<span data-ttu-id="ea4a3-133">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-133">Namespace Name.</span></span>

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

### <span data-ttu-id="ea4a3-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="ea4a3-134">-RegenerateKey</span></span>
<span data-ttu-id="ea4a3-135">Ponownie generuj klucze — "KluczPodstawowy"/"Klucz Pomocniczy".</span><span class="sxs-lookup"><span data-stu-id="ea4a3-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="ea4a3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea4a3-136">-ResourceGroupName</span></span>
<span data-ttu-id="ea4a3-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea4a3-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ea4a3-138">-WcfRelay</span></span>
<span data-ttu-id="ea4a3-139">Nazwa aplikacji WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="ea4a3-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea4a3-140">-Confirm</span></span>
<span data-ttu-id="ea4a3-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea4a3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea4a3-142">-WhatIf</span></span>
<span data-ttu-id="ea4a3-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea4a3-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea4a3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea4a3-145">CommonParameters</span></span>
<span data-ttu-id="ea4a3-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea4a3-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea4a3-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea4a3-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea4a3-148">INPUTS</span></span>

### <span data-ttu-id="ea4a3-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ea4a3-149">System.String</span></span>

## <span data-ttu-id="ea4a3-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea4a3-150">OUTPUTS</span></span>

### <span data-ttu-id="ea4a3-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="ea4a3-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="ea4a3-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ea4a3-152">NOTES</span></span>

## <span data-ttu-id="ea4a3-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea4a3-153">RELATED LINKS</span></span>
