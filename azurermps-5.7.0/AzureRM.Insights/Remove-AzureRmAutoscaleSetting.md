---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 4d6c2f748915847038ef4029dc024763375ef99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542603"
---
# <span data-ttu-id="a464f-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a464f-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="a464f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a464f-102">SYNOPSIS</span></span>
<span data-ttu-id="a464f-103">Usuwa ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="a464f-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a464f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a464f-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a464f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a464f-105">DESCRIPTION</span></span>
<span data-ttu-id="a464f-106">Polecenie cmdlet **Remove-AzureRmAutoscaleSetting** usuwa ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="a464f-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="a464f-107">Musisz określić nazwę ustawienia oraz nazwę grupy zasobów, do której jest przypisana.</span><span class="sxs-lookup"><span data-stu-id="a464f-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

<span data-ttu-id="a464f-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="a464f-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="a464f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a464f-109">EXAMPLES</span></span>

## <span data-ttu-id="a464f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a464f-110">PARAMETERS</span></span>

### <span data-ttu-id="a464f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a464f-111">-DefaultProfile</span></span>
<span data-ttu-id="a464f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a464f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a464f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a464f-113">-Name</span></span>
<span data-ttu-id="a464f-114">Określa nazwę ustawienia skalowania automatycznego, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="a464f-114">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a464f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a464f-115">-ResourceGroupName</span></span>
<span data-ttu-id="a464f-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a464f-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a464f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a464f-117">CommonParameters</span></span>
<span data-ttu-id="a464f-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a464f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a464f-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a464f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a464f-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a464f-120">INPUTS</span></span>

### <span data-ttu-id="a464f-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a464f-121">None</span></span>
<span data-ttu-id="a464f-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a464f-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a464f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a464f-123">OUTPUTS</span></span>

### <span data-ttu-id="a464f-124">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a464f-124">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="a464f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a464f-125">NOTES</span></span>

## <span data-ttu-id="a464f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a464f-126">RELATED LINKS</span></span>

[<span data-ttu-id="a464f-127">Dodaj-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a464f-127">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="a464f-128">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a464f-128">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


