---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: 7ed232d14d215966b6cfad3ba788d3c80938316c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707155"
---
# <span data-ttu-id="0576c-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="0576c-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="0576c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0576c-102">SYNOPSIS</span></span>
<span data-ttu-id="0576c-103">Pobiera historię grup inteligentnych</span><span class="sxs-lookup"><span data-stu-id="0576c-103">Gets smart group history</span></span>

## <span data-ttu-id="0576c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0576c-104">SYNTAX</span></span>

### <span data-ttu-id="0576c-105">BySmartGroupId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0576c-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0576c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0576c-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0576c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0576c-107">DESCRIPTION</span></span>
<span data-ttu-id="0576c-108">Polecenie cmdlet **Get-AzSmartGroupHistory** pobiera historię grup inteligentnych.</span><span class="sxs-lookup"><span data-stu-id="0576c-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="0576c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0576c-109">EXAMPLES</span></span>

### <span data-ttu-id="0576c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0576c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="0576c-111">Pobiera szczegóły historii grupy inteligentnej.</span><span class="sxs-lookup"><span data-stu-id="0576c-111">Gets smart group history details.</span></span>

## <span data-ttu-id="0576c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0576c-112">PARAMETERS</span></span>

### <span data-ttu-id="0576c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0576c-113">-DefaultProfile</span></span>
<span data-ttu-id="0576c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0576c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0576c-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0576c-115">-InputObject</span></span>
<span data-ttu-id="0576c-116">Obiekt wejściowy z potoku.</span><span class="sxs-lookup"><span data-stu-id="0576c-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0576c-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="0576c-117">-SmartGroupId</span></span>
<span data-ttu-id="0576c-118">Unikatowy identyfikator karty inteligentnej/ResourceId alertu.</span><span class="sxs-lookup"><span data-stu-id="0576c-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0576c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0576c-119">CommonParameters</span></span>
<span data-ttu-id="0576c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0576c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0576c-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0576c-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0576c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0576c-122">INPUTS</span></span>

### <span data-ttu-id="0576c-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0576c-123">None</span></span>

## <span data-ttu-id="0576c-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0576c-124">OUTPUTS</span></span>

### <span data-ttu-id="0576c-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="0576c-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="0576c-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0576c-126">NOTES</span></span>

## <span data-ttu-id="0576c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0576c-127">RELATED LINKS</span></span>
