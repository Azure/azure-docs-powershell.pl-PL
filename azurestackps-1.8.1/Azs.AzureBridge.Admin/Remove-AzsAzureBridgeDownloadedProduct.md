---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc5311b1c26d4ae0cb9c1a7ce6ad58a818b53c6
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/22/2020
ms.locfileid: "93899448"
---
# <span data-ttu-id="7f71f-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="7f71f-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="7f71f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f71f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f71f-103">Usuwanie produktu pobranego z usługi Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="7f71f-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="7f71f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f71f-104">SYNTAX</span></span>

### <span data-ttu-id="7f71f-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7f71f-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f71f-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="7f71f-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f71f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7f71f-107">DESCRIPTION</span></span>
<span data-ttu-id="7f71f-108">Usuwanie produktu pobranego z usługi Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="7f71f-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="7f71f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f71f-109">EXAMPLES</span></span>

### <span data-ttu-id="7f71f-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="7f71f-110">EXAMPLE 1</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="7f71f-111">Usuwanie produktu pobranego z usługi Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="7f71f-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="7f71f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f71f-112">PARAMETERS</span></span>

### <span data-ttu-id="7f71f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f71f-113">-Name</span></span>
<span data-ttu-id="7f71f-114">Nazwa produktu.</span><span class="sxs-lookup"><span data-stu-id="7f71f-114">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f71f-115">-Activationname</span><span class="sxs-lookup"><span data-stu-id="7f71f-115">-ActivationName</span></span>
<span data-ttu-id="7f71f-116">Nazwa aktywacji.</span><span class="sxs-lookup"><span data-stu-id="7f71f-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f71f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f71f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f71f-118">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="7f71f-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f71f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7f71f-119">-Force</span></span>
<span data-ttu-id="7f71f-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7f71f-120">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f71f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f71f-121">-ResourceId</span></span>
<span data-ttu-id="7f71f-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="7f71f-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f71f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f71f-123">-AsJob</span></span>
<span data-ttu-id="7f71f-124">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="7f71f-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f71f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f71f-125">-WhatIf</span></span>
<span data-ttu-id="7f71f-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f71f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f71f-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f71f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f71f-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f71f-128">-Confirm</span></span>
<span data-ttu-id="7f71f-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f71f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f71f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f71f-130">CommonParameters</span></span>
<span data-ttu-id="7f71f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f71f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f71f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f71f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f71f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f71f-133">INPUTS</span></span>

## <span data-ttu-id="7f71f-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f71f-134">OUTPUTS</span></span>

### <span data-ttu-id="7f71f-135">Microsoft. AzureStack. Management. AzureBridge. admin. models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="7f71f-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="7f71f-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f71f-136">NOTES</span></span>

## <span data-ttu-id="7f71f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f71f-137">RELATED LINKS</span></span>
