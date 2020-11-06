---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: eaa7cfa9f58bb9bb5affa7a035d194910bcf0006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542604"
---
# <span data-ttu-id="2c6cc-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="2c6cc-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="2c6cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c6cc-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6cc-103">Usuwa regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="2c6cc-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c6cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c6cc-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c6cc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2c6cc-105">DESCRIPTION</span></span>
<span data-ttu-id="2c6cc-106">Polecenie cmdlet **Remove-AzureRmAlertRule** umożliwia usunięcie reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c6cc-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="2c6cc-107">Musisz określić nazwę reguły alertu i grupę zasobów, do której jest przypisana.</span><span class="sxs-lookup"><span data-stu-id="2c6cc-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

<span data-ttu-id="2c6cc-108">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="2c6cc-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2c6cc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c6cc-109">EXAMPLES</span></span>

### <span data-ttu-id="2c6cc-110">Przykład 1: Usuwanie reguły alertu</span><span class="sxs-lookup"><span data-stu-id="2c6cc-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="2c6cc-111">To polecenie usuwa regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8 w grupie zasobów domyślne — Centrala internetowa.</span><span class="sxs-lookup"><span data-stu-id="2c6cc-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="2c6cc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c6cc-112">PARAMETERS</span></span>

### <span data-ttu-id="2c6cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6cc-113">-DefaultProfile</span></span>
<span data-ttu-id="2c6cc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2c6cc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c6cc-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c6cc-115">-Name</span></span>
<span data-ttu-id="2c6cc-116">Określa nazwę reguły alertu, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="2c6cc-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="2c6cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c6cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c6cc-118">Określa nazwę grupy zasobów dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="2c6cc-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="2c6cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6cc-119">CommonParameters</span></span>
<span data-ttu-id="2c6cc-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c6cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6cc-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c6cc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6cc-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c6cc-122">INPUTS</span></span>

### <span data-ttu-id="2c6cc-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2c6cc-123">None</span></span>
<span data-ttu-id="2c6cc-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2c6cc-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2c6cc-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c6cc-125">OUTPUTS</span></span>

### <span data-ttu-id="2c6cc-126">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2c6cc-126">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2c6cc-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c6cc-127">NOTES</span></span>

## <span data-ttu-id="2c6cc-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c6cc-128">RELATED LINKS</span></span>

[<span data-ttu-id="2c6cc-129">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="2c6cc-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="2c6cc-130">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="2c6cc-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="2c6cc-131">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="2c6cc-131">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="2c6cc-132">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="2c6cc-132">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


