---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: 46a3551e309504d9938359a0fed4d37860fcb524
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708151"
---
# <span data-ttu-id="55ae4-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="55ae4-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="55ae4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="55ae4-103">Generuje podstawowe lub pomocnicze ciągi połączeń dla obszaru nazw lub kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="55ae4-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="55ae4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55ae4-104">SYNTAX</span></span>

### <span data-ttu-id="55ae4-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="55ae4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55ae4-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="55ae4-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55ae4-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="55ae4-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55ae4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="55ae4-108">DESCRIPTION</span></span>
<span data-ttu-id="55ae4-109">Polecenie cmdlet **New-AzServiceBusKey** generuje nowe podstawowe lub pomocnicze ciągi połączeń dla określonego obszaru nazw, kolejki lub tematu oraz reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="55ae4-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="55ae4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55ae4-110">EXAMPLES</span></span>

### <span data-ttu-id="55ae4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="55ae4-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="55ae4-112">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="55ae4-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="55ae4-113">Przykład 1,1</span><span class="sxs-lookup"><span data-stu-id="55ae4-113">Example 1.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="55ae4-114">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia z podaną wartością klucza dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="55ae4-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="55ae4-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="55ae4-115">Example 2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="55ae4-116">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla kolejki.</span><span class="sxs-lookup"><span data-stu-id="55ae4-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="55ae4-117">Przykład 2,2</span><span class="sxs-lookup"><span data-stu-id="55ae4-117">Example 2.2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="55ae4-118">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia z podaną wartością klucza kolejki.</span><span class="sxs-lookup"><span data-stu-id="55ae4-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="55ae4-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="55ae4-119">Example 3</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="55ae4-120">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla tematu.</span><span class="sxs-lookup"><span data-stu-id="55ae4-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="55ae4-121">Przykład 3,1</span><span class="sxs-lookup"><span data-stu-id="55ae4-121">Example 3.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="55ae4-122">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia z podaną wartością klucza tematu.</span><span class="sxs-lookup"><span data-stu-id="55ae4-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="55ae4-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55ae4-123">PARAMETERS</span></span>

### <span data-ttu-id="55ae4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ae4-124">-DefaultProfile</span></span>
<span data-ttu-id="55ae4-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55ae4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55ae4-126">-Wartość parametru</span><span class="sxs-lookup"><span data-stu-id="55ae4-126">-KeyValue</span></span>
<span data-ttu-id="55ae4-127">Zakodowany algorytm Base64 256-bitowy klucz do podpisywania i sprawdzania poprawności tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="55ae4-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="55ae4-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="55ae4-128">-Name</span></span>
<span data-ttu-id="55ae4-129">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="55ae4-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="55ae4-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="55ae4-130">-Namespace</span></span>
<span data-ttu-id="55ae4-131">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="55ae4-131">Namespace Name</span></span>

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

### <span data-ttu-id="55ae4-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="55ae4-132">-Queue</span></span>
<span data-ttu-id="55ae4-133">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="55ae4-133">Queue Name</span></span>

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

### <span data-ttu-id="55ae4-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="55ae4-134">-RegenerateKey</span></span>
<span data-ttu-id="55ae4-135">Ponowne generowanie kluczy — "Primarykea"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="55ae4-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="55ae4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ae4-136">-ResourceGroupName</span></span>
<span data-ttu-id="55ae4-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="55ae4-137">Resource Group Name</span></span>

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

### <span data-ttu-id="55ae4-138">— Temat</span><span class="sxs-lookup"><span data-stu-id="55ae4-138">-Topic</span></span>
<span data-ttu-id="55ae4-139">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="55ae4-139">Topic Name</span></span>

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

### <span data-ttu-id="55ae4-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="55ae4-140">-Confirm</span></span>
<span data-ttu-id="55ae4-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55ae4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55ae4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55ae4-142">-WhatIf</span></span>
<span data-ttu-id="55ae4-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55ae4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55ae4-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="55ae4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55ae4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ae4-145">CommonParameters</span></span>
<span data-ttu-id="55ae4-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55ae4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ae4-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55ae4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ae4-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55ae4-148">INPUTS</span></span>

### <span data-ttu-id="55ae4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="55ae4-149">System.String</span></span>

## <span data-ttu-id="55ae4-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55ae4-150">OUTPUTS</span></span>

### <span data-ttu-id="55ae4-151">Microsoft. Azure. Commands. ServiceBus. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="55ae4-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="55ae4-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55ae4-152">NOTES</span></span>

## <span data-ttu-id="55ae4-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55ae4-153">RELATED LINKS</span></span>
