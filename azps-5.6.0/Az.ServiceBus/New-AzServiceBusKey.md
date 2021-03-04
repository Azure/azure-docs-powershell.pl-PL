---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: ac3b98089a3bbb710680269692685a32ef7adc03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950954"
---
# <span data-ttu-id="de8c9-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="de8c9-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="de8c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="de8c9-103">Ponowne generowanie podstawowych lub pomocniczych ciągów połączenia dla przestrzeni nazw, kolejki lub tematu autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="de8c9-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="de8c9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de8c9-104">SYNTAX</span></span>

### <span data-ttu-id="de8c9-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="de8c9-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de8c9-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="de8c9-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de8c9-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="de8c9-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de8c9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="de8c9-108">DESCRIPTION</span></span>
<span data-ttu-id="de8c9-109">Polecenie **cmdlet New-AzServiceBusKey** generuje nowe podstawowe lub pomocnicze parametry połączenia dla określonej przestrzeni nazw, kolejki lub tematu i reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="de8c9-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="de8c9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de8c9-110">EXAMPLES</span></span>

### <span data-ttu-id="de8c9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de8c9-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="de8c9-112">Ponowne generowanie podstawowych lub pomocniczych ciągów połączenia dla przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="de8c9-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="de8c9-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="de8c9-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="de8c9-114">Ponowne generowanie podstawowych lub pomocniczych ciągów połączenia przy użyciu podanej wartości klucza dla przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="de8c9-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="de8c9-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="de8c9-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="de8c9-116">Ponowne generowanie podstawowych lub pomocniczych ciągów połączeń dla kolejki.</span><span class="sxs-lookup"><span data-stu-id="de8c9-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="de8c9-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="de8c9-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="de8c9-118">Ponownie generuje podstawowe lub pomocnicze parametry połączenia przy użyciu podanej wartości klucza dla kolejki.</span><span class="sxs-lookup"><span data-stu-id="de8c9-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="de8c9-119">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="de8c9-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="de8c9-120">Ponowne generowanie podstawowych lub pomocniczych ciągów połączeń dla tematu.</span><span class="sxs-lookup"><span data-stu-id="de8c9-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="de8c9-121">Przykład 6</span><span class="sxs-lookup"><span data-stu-id="de8c9-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="de8c9-122">Ponowne generowanie podstawowych lub pomocniczych ciągów połączeń z podaną wartością klucza tematu.</span><span class="sxs-lookup"><span data-stu-id="de8c9-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="de8c9-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de8c9-123">PARAMETERS</span></span>

### <span data-ttu-id="de8c9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8c9-124">-DefaultProfile</span></span>
<span data-ttu-id="de8c9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de8c9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de8c9-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="de8c9-126">-KeyValue</span></span>
<span data-ttu-id="de8c9-127">Zakodowany w bazie danych klucz 256-bitowy do podpisywania i sprawdzania poprawności tokenu SAS.</span><span class="sxs-lookup"><span data-stu-id="de8c9-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="de8c9-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="de8c9-128">-Name</span></span>
<span data-ttu-id="de8c9-129">Nazwa podmiotu autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="de8c9-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="de8c9-130">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="de8c9-130">-Namespace</span></span>
<span data-ttu-id="de8c9-131">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="de8c9-131">Namespace Name</span></span>

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

### <span data-ttu-id="de8c9-132">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="de8c9-132">-Queue</span></span>
<span data-ttu-id="de8c9-133">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="de8c9-133">Queue Name</span></span>

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

### <span data-ttu-id="de8c9-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="de8c9-134">-RegenerateKey</span></span>
<span data-ttu-id="de8c9-135">Ponownie generuj klucze — "KluczPodstawowy"/"Klucz Pomocniczy".</span><span class="sxs-lookup"><span data-stu-id="de8c9-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="de8c9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de8c9-136">-ResourceGroupName</span></span>
<span data-ttu-id="de8c9-137">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="de8c9-137">Resource Group Name</span></span>

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

### <span data-ttu-id="de8c9-138">— Temat</span><span class="sxs-lookup"><span data-stu-id="de8c9-138">-Topic</span></span>
<span data-ttu-id="de8c9-139">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="de8c9-139">Topic Name</span></span>

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

### <span data-ttu-id="de8c9-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de8c9-140">-Confirm</span></span>
<span data-ttu-id="de8c9-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="de8c9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de8c9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de8c9-142">-WhatIf</span></span>
<span data-ttu-id="de8c9-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de8c9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de8c9-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="de8c9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de8c9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8c9-145">CommonParameters</span></span>
<span data-ttu-id="de8c9-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de8c9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8c9-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de8c9-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8c9-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de8c9-148">INPUTS</span></span>

### <span data-ttu-id="de8c9-149">System.String</span><span class="sxs-lookup"><span data-stu-id="de8c9-149">System.String</span></span>

## <span data-ttu-id="de8c9-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de8c9-150">OUTPUTS</span></span>

### <span data-ttu-id="de8c9-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="de8c9-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="de8c9-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de8c9-152">NOTES</span></span>

## <span data-ttu-id="de8c9-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de8c9-153">RELATED LINKS</span></span>
