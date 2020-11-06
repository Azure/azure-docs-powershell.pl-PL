---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 6efd58497adc1e59f1bf6d2c2151386ee773f66a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550216"
---
# <span data-ttu-id="8551c-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="8551c-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="8551c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8551c-102">SYNOPSIS</span></span>
<span data-ttu-id="8551c-103">Generuje podstawowe lub pomocnicze ciągi połączeń dla obszaru nazw lub kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="8551c-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8551c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8551c-104">SYNTAX</span></span>

### <span data-ttu-id="8551c-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8551c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8551c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8551c-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8551c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8551c-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8551c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8551c-108">DESCRIPTION</span></span>
<span data-ttu-id="8551c-109">Polecenie cmdlet **New-AzureRmServiceBusKey** generuje nowe podstawowe lub pomocnicze ciągi połączeń dla określonego obszaru nazw, kolejki lub tematu oraz reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="8551c-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="8551c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8551c-110">EXAMPLES</span></span>

### <span data-ttu-id="8551c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8551c-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="8551c-112">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="8551c-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="8551c-113">Przykład 1,1</span><span class="sxs-lookup"><span data-stu-id="8551c-113">Example 1.1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="8551c-114">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia z podaną wartością klucza dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="8551c-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="8551c-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8551c-115">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="8551c-116">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla kolejki.</span><span class="sxs-lookup"><span data-stu-id="8551c-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="8551c-117">Przykład 2,2</span><span class="sxs-lookup"><span data-stu-id="8551c-117">Example 2.2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="8551c-118">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia z podaną wartością klucza kolejki.</span><span class="sxs-lookup"><span data-stu-id="8551c-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="8551c-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8551c-119">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="8551c-120">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla tematu.</span><span class="sxs-lookup"><span data-stu-id="8551c-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="8551c-121">Przykład 3,1</span><span class="sxs-lookup"><span data-stu-id="8551c-121">Example 3.1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="8551c-122">Generuje ponownie podstawowy lub pomocniczy ciąg połączenia z podaną wartością klucza tematu.</span><span class="sxs-lookup"><span data-stu-id="8551c-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="8551c-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8551c-123">PARAMETERS</span></span>

### <span data-ttu-id="8551c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8551c-124">-DefaultProfile</span></span>
<span data-ttu-id="8551c-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8551c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8551c-126">-Wartość parametru</span><span class="sxs-lookup"><span data-stu-id="8551c-126">-KeyValue</span></span>
<span data-ttu-id="8551c-127">Zakodowany algorytm Base64 256-bitowy klucz do podpisywania i sprawdzania poprawności tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="8551c-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="8551c-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8551c-128">-Name</span></span>
<span data-ttu-id="8551c-129">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="8551c-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="8551c-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8551c-130">-Namespace</span></span>
<span data-ttu-id="8551c-131">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="8551c-131">Namespace Name</span></span>

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

### <span data-ttu-id="8551c-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="8551c-132">-Queue</span></span>
<span data-ttu-id="8551c-133">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="8551c-133">Queue Name</span></span>

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

### <span data-ttu-id="8551c-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="8551c-134">-RegenerateKey</span></span>
<span data-ttu-id="8551c-135">Ponowne generowanie kluczy — "Primarykea"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="8551c-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="8551c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8551c-136">-ResourceGroupName</span></span>
<span data-ttu-id="8551c-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8551c-137">Resource Group Name</span></span>

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

### <span data-ttu-id="8551c-138">— Temat</span><span class="sxs-lookup"><span data-stu-id="8551c-138">-Topic</span></span>
<span data-ttu-id="8551c-139">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="8551c-139">Topic Name</span></span>

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

### <span data-ttu-id="8551c-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8551c-140">-Confirm</span></span>
<span data-ttu-id="8551c-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8551c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8551c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8551c-142">-WhatIf</span></span>
<span data-ttu-id="8551c-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8551c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8551c-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8551c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8551c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8551c-145">CommonParameters</span></span>
<span data-ttu-id="8551c-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8551c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8551c-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8551c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8551c-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8551c-148">INPUTS</span></span>

### <span data-ttu-id="8551c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8551c-149">System.String</span></span>

## <span data-ttu-id="8551c-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8551c-150">OUTPUTS</span></span>

### <span data-ttu-id="8551c-151">Microsoft. Azure. Commands. ServiceBus. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="8551c-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="8551c-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8551c-152">NOTES</span></span>

## <span data-ttu-id="8551c-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8551c-153">RELATED LINKS</span></span>
