---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: c0c413918a986da4eaea8d9ef5f0f6a091b8b2e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502909"
---
# <span data-ttu-id="969f4-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="969f4-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="969f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="969f4-102">SYNOPSIS</span></span>
<span data-ttu-id="969f4-103">Generuje podstawowe lub pomocnicze ciągi połączeń dla obszaru nazw lub kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="969f4-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="969f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="969f4-104">SYNTAX</span></span>

### <span data-ttu-id="969f4-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="969f4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="969f4-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="969f4-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="969f4-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="969f4-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="969f4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="969f4-108">DESCRIPTION</span></span>
<span data-ttu-id="969f4-109">Polecenie cmdlet **New-AzServiceBusKey** generuje nowe podstawowe lub pomocnicze ciągi połączeń dla określonego obszaru nazw, kolejki lub tematu oraz reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="969f4-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="969f4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="969f4-110">EXAMPLES</span></span>

### <span data-ttu-id="969f4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="969f4-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="969f4-112">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="969f4-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="969f4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="969f4-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="969f4-114">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia z podaną wartością klucza dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="969f4-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="969f4-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="969f4-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="969f4-116">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla kolejki.</span><span class="sxs-lookup"><span data-stu-id="969f4-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="969f4-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="969f4-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="969f4-118">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia z podaną wartością klucza kolejki.</span><span class="sxs-lookup"><span data-stu-id="969f4-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="969f4-119">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="969f4-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="969f4-120">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla tematu.</span><span class="sxs-lookup"><span data-stu-id="969f4-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="969f4-121">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="969f4-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="969f4-122">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia z podaną wartością klucza tematu.</span><span class="sxs-lookup"><span data-stu-id="969f4-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="969f4-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="969f4-123">PARAMETERS</span></span>

### <span data-ttu-id="969f4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969f4-124">-DefaultProfile</span></span>
<span data-ttu-id="969f4-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="969f4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="969f4-126">-Wartość parametru</span><span class="sxs-lookup"><span data-stu-id="969f4-126">-KeyValue</span></span>
<span data-ttu-id="969f4-127">Zakodowany algorytm Base64 256-bitowy klucz do podpisywania i sprawdzania poprawności tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="969f4-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="969f4-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="969f4-128">-Name</span></span>
<span data-ttu-id="969f4-129">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="969f4-129">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969f4-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="969f4-130">-Namespace</span></span>
<span data-ttu-id="969f4-131">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="969f4-131">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969f4-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="969f4-132">-Queue</span></span>
<span data-ttu-id="969f4-133">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="969f4-133">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969f4-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="969f4-134">-RegenerateKey</span></span>
<span data-ttu-id="969f4-135">Ponowne generowanie kluczy — "Primarykea"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="969f4-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969f4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969f4-136">-ResourceGroupName</span></span>
<span data-ttu-id="969f4-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="969f4-137">Resource Group Name</span></span>

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

### <span data-ttu-id="969f4-138">— Temat</span><span class="sxs-lookup"><span data-stu-id="969f4-138">-Topic</span></span>
<span data-ttu-id="969f4-139">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="969f4-139">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969f4-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="969f4-140">-Confirm</span></span>
<span data-ttu-id="969f4-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="969f4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="969f4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969f4-142">-WhatIf</span></span>
<span data-ttu-id="969f4-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="969f4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="969f4-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="969f4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="969f4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969f4-145">CommonParameters</span></span>
<span data-ttu-id="969f4-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969f4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969f4-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969f4-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969f4-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="969f4-148">INPUTS</span></span>

### <span data-ttu-id="969f4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="969f4-149">System.String</span></span>

## <span data-ttu-id="969f4-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="969f4-150">OUTPUTS</span></span>

### <span data-ttu-id="969f4-151">Microsoft. Azure. Commands. ServiceBus. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="969f4-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="969f4-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="969f4-152">NOTES</span></span>

## <span data-ttu-id="969f4-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="969f4-153">RELATED LINKS</span></span>
