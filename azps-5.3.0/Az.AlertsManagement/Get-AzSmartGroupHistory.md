---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502570"
---
# <span data-ttu-id="9c4b7-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="9c4b7-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="9c4b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="9c4b7-103">Pobiera historię grup inteligentnych</span><span class="sxs-lookup"><span data-stu-id="9c4b7-103">Gets smart group history</span></span>

## <span data-ttu-id="9c4b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c4b7-104">SYNTAX</span></span>

### <span data-ttu-id="9c4b7-105">BySmartGroupId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9c4b7-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c4b7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9c4b7-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c4b7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9c4b7-107">DESCRIPTION</span></span>
<span data-ttu-id="9c4b7-108">Polecenie cmdlet **Get-AzSmartGroupHistory** pobiera historię grup inteligentnych.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="9c4b7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c4b7-109">EXAMPLES</span></span>

### <span data-ttu-id="9c4b7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c4b7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="9c4b7-111">Pobiera szczegóły historii grupy inteligentnej.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-111">Gets smart group history details.</span></span>

## <span data-ttu-id="9c4b7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c4b7-112">PARAMETERS</span></span>

### <span data-ttu-id="9c4b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c4b7-113">-DefaultProfile</span></span>
<span data-ttu-id="9c4b7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c4b7-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9c4b7-115">-InputObject</span></span>
<span data-ttu-id="9c4b7-116">Obiekt wejściowy z potoku.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="9c4b7-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="9c4b7-117">-SmartGroupId</span></span>
<span data-ttu-id="9c4b7-118">Unikatowy identyfikator karty inteligentnej/ResourceId alertu.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="9c4b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c4b7-119">CommonParameters</span></span>
<span data-ttu-id="9c4b7-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c4b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c4b7-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c4b7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c4b7-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c4b7-122">INPUTS</span></span>

### <span data-ttu-id="9c4b7-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9c4b7-123">None</span></span>

## <span data-ttu-id="9c4b7-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c4b7-124">OUTPUTS</span></span>

### <span data-ttu-id="9c4b7-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="9c4b7-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="9c4b7-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c4b7-126">NOTES</span></span>

## <span data-ttu-id="9c4b7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c4b7-127">RELATED LINKS</span></span>
