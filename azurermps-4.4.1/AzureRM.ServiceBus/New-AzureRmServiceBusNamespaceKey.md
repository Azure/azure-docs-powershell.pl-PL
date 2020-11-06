---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 5b366a3be8ca715a42c1c1f916d8ebf327dff8fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549851"
---
# <span data-ttu-id="29ccd-101">New-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="29ccd-101">New-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="29ccd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="29ccd-103">Generuje podstawowe lub pomocnicze ciągi połączeń dla obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="29ccd-103">Regenerates the primary or secondary connection strings for the Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29ccd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29ccd-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29ccd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29ccd-105">DESCRIPTION</span></span>
<span data-ttu-id="29ccd-106">Polecenie cmdlet **New-AzureRmServiceBusNamespace** generuje nowe podstawowe lub pomocnicze ciągi połączeń dla określonego obszaru nazw i reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="29ccd-106">The **New-AzureRmServiceBusNamespace** cmdlet generates new primary or secondary connection strings for the specified namespace and authorization rule.</span></span>

## <span data-ttu-id="29ccd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29ccd-107">EXAMPLES</span></span>

### <span data-ttu-id="29ccd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="29ccd-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="29ccd-109">Regeneruje podstawowy lub pomocniczy ciąg połączenia dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="29ccd-109">Regenerates the primary or secondary connection strings for the namespace.</span></span>

## <span data-ttu-id="29ccd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29ccd-110">PARAMETERS</span></span>

### <span data-ttu-id="29ccd-111">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="29ccd-111">-RegenerateKeys</span></span>
<span data-ttu-id="29ccd-112">Ponowne generowanie kluczy: Primarykea/SecondaryKey.</span><span class="sxs-lookup"><span data-stu-id="29ccd-112">Regenerate Keys: PrimaryKey/SecondaryKey.</span></span>

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

### <span data-ttu-id="29ccd-113">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="29ccd-113">-ResourceGroup</span></span>
<span data-ttu-id="29ccd-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="29ccd-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ccd-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29ccd-115">-Confirm</span></span>
<span data-ttu-id="29ccd-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29ccd-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ccd-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29ccd-117">-WhatIf</span></span>
<span data-ttu-id="29ccd-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29ccd-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29ccd-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29ccd-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ccd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ccd-120">-DefaultProfile</span></span>
<span data-ttu-id="29ccd-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29ccd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29ccd-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29ccd-122">-Name</span></span>
<span data-ttu-id="29ccd-123">Nazwa reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="29ccd-123">Authorization Rule Name.</span></span>

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

### <span data-ttu-id="29ccd-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="29ccd-124">-Namespace</span></span>
<span data-ttu-id="29ccd-125">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="29ccd-125">Namespace Name.</span></span>

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

### <span data-ttu-id="29ccd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ccd-126">CommonParameters</span></span>
<span data-ttu-id="29ccd-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29ccd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ccd-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29ccd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ccd-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29ccd-129">INPUTS</span></span>

### <span data-ttu-id="29ccd-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="29ccd-130">-ResourceGroup</span></span>
 <span data-ttu-id="29ccd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="29ccd-131">System.String</span></span>
 

### <span data-ttu-id="29ccd-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="29ccd-132">-NamespaceName</span></span>
 <span data-ttu-id="29ccd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="29ccd-133">System.String</span></span>
 

### <span data-ttu-id="29ccd-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="29ccd-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="29ccd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="29ccd-135">System.String</span></span>
 

### <span data-ttu-id="29ccd-136">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="29ccd-136">-RegenerateKeys</span></span>
 <span data-ttu-id="29ccd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="29ccd-137">System.String</span></span>

## <span data-ttu-id="29ccd-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29ccd-138">OUTPUTS</span></span>

### <span data-ttu-id="29ccd-139">Microsoft. Azure. Management. ServiceBus. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="29ccd-139">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="29ccd-140">PrimaryConnectionString: punkt końcowy = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Value} SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.NET/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Value} PrimaryKey: {wartość PrimaryKey} SecondaryKey: {SecondaryKey wartość} NazwaKlucza: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="29ccd-140">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="29ccd-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29ccd-141">NOTES</span></span>

## <span data-ttu-id="29ccd-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29ccd-142">RELATED LINKS</span></span>

