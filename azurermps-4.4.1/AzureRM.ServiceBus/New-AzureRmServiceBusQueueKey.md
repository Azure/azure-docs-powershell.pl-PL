---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719242"
---
# <span data-ttu-id="58650-101">New-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="58650-101">New-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="58650-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58650-102">SYNOPSIS</span></span>
<span data-ttu-id="58650-103">Generuje podstawowe lub pomocnicze ciągi połączeń dla kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="58650-103">Regenerates the primary or secondary connection strings for the Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58650-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58650-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58650-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58650-105">DESCRIPTION</span></span>
<span data-ttu-id="58650-106">Polecenie cmdlet **New-AzureRmServiceBusQueueKey** generuje ponownie podstawowy lub pomocniczy ciąg połączenia dla określonej kolejki usługi Service Bus i reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="58650-106">The **New-AzureRmServiceBusQueueKey** cmdlet regenerates the primary or secondary connection strings for the specified Service Bus queue and authorization rule.</span></span>

## <span data-ttu-id="58650-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58650-107">EXAMPLES</span></span>

### <span data-ttu-id="58650-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58650-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="58650-109">Generuje ponownie główne parametry połączenia dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="58650-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="58650-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="58650-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="58650-111">Generuje ponownie parametry połączenia pomocniczego dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="58650-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="58650-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58650-112">PARAMETERS</span></span>

### <span data-ttu-id="58650-113">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="58650-113">-AuthorizationRuleName</span></span>
<span data-ttu-id="58650-114">Nazwa reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="58650-114">The authorization rule name.</span></span>

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

### <span data-ttu-id="58650-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="58650-115">-NamespaceName</span></span>
<span data-ttu-id="58650-116">Nazwa obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="58650-116">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58650-117">-QueueName</span><span class="sxs-lookup"><span data-stu-id="58650-117">-QueueName</span></span>
<span data-ttu-id="58650-118">Nazwa kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="58650-118">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58650-119">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="58650-119">-RegenerateKeys</span></span>
<span data-ttu-id="58650-120">Określa, czy ponownie wygenerować klucze podstawowe i pomocnicze.</span><span class="sxs-lookup"><span data-stu-id="58650-120">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58650-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="58650-121">-ResourceGroup</span></span>
<span data-ttu-id="58650-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58650-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="58650-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58650-123">-Confirm</span></span>
<span data-ttu-id="58650-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58650-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58650-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58650-125">-WhatIf</span></span>
<span data-ttu-id="58650-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58650-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58650-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58650-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58650-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58650-128">CommonParameters</span></span>
<span data-ttu-id="58650-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58650-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58650-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58650-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58650-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58650-131">INPUTS</span></span>

### <span data-ttu-id="58650-132">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="58650-132">-ResourceGroup</span></span>
 <span data-ttu-id="58650-133">System. String</span><span class="sxs-lookup"><span data-stu-id="58650-133">System.String</span></span>
 

### <span data-ttu-id="58650-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="58650-134">-NamespaceName</span></span>
 <span data-ttu-id="58650-135">System. String</span><span class="sxs-lookup"><span data-stu-id="58650-135">System.String</span></span>
 

### <span data-ttu-id="58650-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="58650-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="58650-137">System. String</span><span class="sxs-lookup"><span data-stu-id="58650-137">System.String</span></span>
 

### <span data-ttu-id="58650-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="58650-138">-QueueName</span></span>
 <span data-ttu-id="58650-139">System. String</span><span class="sxs-lookup"><span data-stu-id="58650-139">System.String</span></span>
 

### <span data-ttu-id="58650-140">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="58650-140">-RegenerateKeys</span></span>
 <span data-ttu-id="58650-141">System. String</span><span class="sxs-lookup"><span data-stu-id="58650-141">System.String</span></span>

## <span data-ttu-id="58650-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58650-142">OUTPUTS</span></span>

### <span data-ttu-id="58650-143">Microsoft. Azure. Management. ServiceBus. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="58650-143">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="58650-144">PrimaryConnectionString: punkt końcowy = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_exa mpl1 PrimaryKey: {wartość PrimaryKey} SecondaryKey: {SecondaryKey wartość} NazwaKlucza: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="58650-144">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="58650-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58650-145">NOTES</span></span>

## <span data-ttu-id="58650-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58650-146">RELATED LINKS</span></span>

