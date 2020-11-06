---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: de0c1f8fa66b195452d7f2c9447189b4e925136b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550996"
---
# <span data-ttu-id="44f93-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="44f93-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="44f93-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44f93-102">SYNOPSIS</span></span>
<span data-ttu-id="44f93-103">Usuwa regułę alertu.</span><span class="sxs-lookup"><span data-stu-id="44f93-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44f93-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44f93-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44f93-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44f93-105">DESCRIPTION</span></span>
<span data-ttu-id="44f93-106">Polecenie cmdlet **Remove-AzureRmAlertRule** umożliwia usunięcie reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="44f93-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="44f93-107">Musisz określić nazwę reguły alertu i grupę zasobów, do której jest przypisana.</span><span class="sxs-lookup"><span data-stu-id="44f93-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

## <span data-ttu-id="44f93-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44f93-108">EXAMPLES</span></span>

### <span data-ttu-id="44f93-109">Przykład 1: Usuwanie reguły alertu</span><span class="sxs-lookup"><span data-stu-id="44f93-109">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="44f93-110">To polecenie usuwa regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8 w grupie zasobów domyślne — Centrala internetowa.</span><span class="sxs-lookup"><span data-stu-id="44f93-110">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="44f93-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44f93-111">PARAMETERS</span></span>

### <span data-ttu-id="44f93-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44f93-112">-Name</span></span>
<span data-ttu-id="44f93-113">Określa nazwę reguły alertu, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="44f93-113">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44f93-114">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="44f93-114">-ResourceGroup</span></span>
<span data-ttu-id="44f93-115">Określa nazwę grupy zasobów dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="44f93-115">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44f93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f93-116">-DefaultProfile</span></span>
<span data-ttu-id="44f93-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44f93-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44f93-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f93-118">CommonParameters</span></span>
<span data-ttu-id="44f93-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44f93-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f93-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44f93-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f93-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44f93-121">INPUTS</span></span>

## <span data-ttu-id="44f93-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44f93-122">OUTPUTS</span></span>

### <span data-ttu-id="44f93-123">System. Collections. Generic. list "1 [Microsoft. Azure. AzureOperationResponse]</span><span class="sxs-lookup"><span data-stu-id="44f93-123">System.Collections.Generic.List\`1[Microsoft.Azure.AzureOperationResponse]</span></span>

## <span data-ttu-id="44f93-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44f93-124">NOTES</span></span>

## <span data-ttu-id="44f93-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44f93-125">RELATED LINKS</span></span>

[<span data-ttu-id="44f93-126">Dodaj-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="44f93-126">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="44f93-127">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="44f93-127">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="44f93-128">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="44f93-128">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="44f93-129">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="44f93-129">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="44f93-130">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="44f93-130">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


