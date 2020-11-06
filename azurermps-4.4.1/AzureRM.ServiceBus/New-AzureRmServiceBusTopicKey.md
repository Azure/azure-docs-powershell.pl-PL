---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542972"
---
# <span data-ttu-id="02641-101">New-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="02641-101">New-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="02641-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02641-102">SYNOPSIS</span></span>
<span data-ttu-id="02641-103">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla tematu Magistrala usług.</span><span class="sxs-lookup"><span data-stu-id="02641-103">Regenerates the primary or secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02641-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02641-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02641-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02641-105">DESCRIPTION</span></span>
<span data-ttu-id="02641-106">Polecenie cmdlet **New-AzureRmServiceBusTopicKey** generuje nowe główne lub pomocnicze parametry połączenia dla określonego tematu magistrali usług i reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="02641-106">The **New-AzureRmServiceBusTopicKey** cmdlet generates a new primary or secondary connection string for the specified Service Bus topic and authorization rule.</span></span>

## <span data-ttu-id="02641-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02641-107">EXAMPLES</span></span>

### <span data-ttu-id="02641-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="02641-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="02641-109">Generuje ponownie główne parametry połączenia dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="02641-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="02641-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="02641-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="02641-111">Generuje ponownie parametry połączenia pomocniczego dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="02641-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="02641-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02641-112">PARAMETERS</span></span>

### <span data-ttu-id="02641-113">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="02641-113">-RegenerateKeys</span></span>
<span data-ttu-id="02641-114">Określa, czy ponownie wygenerować klucze podstawowe i pomocnicze.</span><span class="sxs-lookup"><span data-stu-id="02641-114">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02641-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="02641-115">-ResourceGroup</span></span>
<span data-ttu-id="02641-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02641-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="02641-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02641-117">-Confirm</span></span>
<span data-ttu-id="02641-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02641-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02641-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02641-119">-WhatIf</span></span>
<span data-ttu-id="02641-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02641-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02641-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02641-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02641-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02641-122">-DefaultProfile</span></span>
<span data-ttu-id="02641-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02641-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02641-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02641-124">-Name</span></span>
<span data-ttu-id="02641-125">Nazwa reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="02641-125">Authorization Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02641-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="02641-126">-Namespace</span></span>
<span data-ttu-id="02641-127">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="02641-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02641-128">— Temat</span><span class="sxs-lookup"><span data-stu-id="02641-128">-Topic</span></span>
<span data-ttu-id="02641-129">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="02641-129">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02641-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02641-130">CommonParameters</span></span>
<span data-ttu-id="02641-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02641-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02641-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02641-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02641-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02641-133">INPUTS</span></span>

### <span data-ttu-id="02641-134">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="02641-134">-ResourceGroup</span></span>
 <span data-ttu-id="02641-135">System. String</span><span class="sxs-lookup"><span data-stu-id="02641-135">System.String</span></span>
 

### <span data-ttu-id="02641-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="02641-136">-NamespaceName</span></span>
 <span data-ttu-id="02641-137">System. String</span><span class="sxs-lookup"><span data-stu-id="02641-137">System.String</span></span>
 

### <span data-ttu-id="02641-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="02641-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="02641-139">System. String</span><span class="sxs-lookup"><span data-stu-id="02641-139">System.String</span></span>
 

### <span data-ttu-id="02641-140">-Tematname</span><span class="sxs-lookup"><span data-stu-id="02641-140">-TopicName</span></span>
 <span data-ttu-id="02641-141">System. String</span><span class="sxs-lookup"><span data-stu-id="02641-141">System.String</span></span>
 

### <span data-ttu-id="02641-142">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="02641-142">-RegenerateKeys</span></span>
 <span data-ttu-id="02641-143">System. String</span><span class="sxs-lookup"><span data-stu-id="02641-143">System.String</span></span>

## <span data-ttu-id="02641-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02641-144">OUTPUTS</span></span>

### <span data-ttu-id="02641-145">Microsoft. Azure. Commands. ServiceBus. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="02641-145">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="02641-146">PrimaryConnectionString: punkt końcowy = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-topi c_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-topi c_exampl1 PrimaryKey: {wartość PrimaryKey} SecondaryKey: {SecondaryKey wartość} NazwaKlucza: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="02641-146">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="02641-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02641-147">NOTES</span></span>

## <span data-ttu-id="02641-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02641-148">RELATED LINKS</span></span>

