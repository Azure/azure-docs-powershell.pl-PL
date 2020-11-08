---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d47f93addf05af19b523db6ba454443af2c34f
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/26/2020
ms.locfileid: "94061794"
---
# <span data-ttu-id="e6ddc-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="e6ddc-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="e6ddc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ddc-103">Zwraca aktywację mostka Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="e6ddc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6ddc-104">SYNTAX</span></span>

### <span data-ttu-id="e6ddc-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e6ddc-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e6ddc-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="e6ddc-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="e6ddc-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e6ddc-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e6ddc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e6ddc-108">DESCRIPTION</span></span>
<span data-ttu-id="e6ddc-109">Po zarejestrowaniu stosu platformy Azure obiekt aktywacji zawiera informacje, które łączą wdrożenie stosu platformy Azure do swojej rejestracji na platformie Azure, na przykład datę wygaśnięcia rejestracji, nazwę itd.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="e6ddc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6ddc-110">EXAMPLES</span></span>

### <span data-ttu-id="e6ddc-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e6ddc-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="e6ddc-112">Uzyskiwanie listy aktywacji usługi Azure Bridge w grupie zasobów "activationRG"</span><span class="sxs-lookup"><span data-stu-id="e6ddc-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="e6ddc-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e6ddc-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="e6ddc-114">Uzyskiwanie aktywacji usługi Azure Bridge na podstawie nazwy "Moja Aktywacja" znajdującej się w obszarze "activationRG"</span><span class="sxs-lookup"><span data-stu-id="e6ddc-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="e6ddc-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6ddc-115">PARAMETERS</span></span>

### <span data-ttu-id="e6ddc-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e6ddc-116">-Name</span></span>
<span data-ttu-id="e6ddc-117">Nazwa aktywacji.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ddc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ddc-118">-ResourceGroupName</span></span>
<span data-ttu-id="e6ddc-119">Grupa zasobów używana podczas rejestracji stosu platformy Azure; Możesz również wyświetlić nazwy grup zasobów w portalu.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ddc-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6ddc-120">-ResourceId</span></span>
<span data-ttu-id="e6ddc-121">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-121">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ddc-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="e6ddc-122">-Skip</span></span>
<span data-ttu-id="e6ddc-123">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ddc-124">-Początek</span><span class="sxs-lookup"><span data-stu-id="e6ddc-124">-Top</span></span>
<span data-ttu-id="e6ddc-125">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e6ddc-126">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ddc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ddc-127">CommonParameters</span></span>
<span data-ttu-id="e6ddc-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ddc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ddc-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6ddc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ddc-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6ddc-130">INPUTS</span></span>

## <span data-ttu-id="e6ddc-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6ddc-131">OUTPUTS</span></span>

### <span data-ttu-id="e6ddc-132">Microsoft. AzureStack. Management. AzureBridge. admin. models. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="e6ddc-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="e6ddc-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6ddc-133">NOTES</span></span>

## <span data-ttu-id="e6ddc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6ddc-134">RELATED LINKS</span></span>

