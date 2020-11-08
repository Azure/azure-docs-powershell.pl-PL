---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225451"
---
# <span data-ttu-id="1d74d-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="1d74d-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="1d74d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d74d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d74d-103">Pobiera informacje o historii alertu</span><span class="sxs-lookup"><span data-stu-id="1d74d-103">Gets Alert History information</span></span>

## <span data-ttu-id="1d74d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d74d-104">SYNTAX</span></span>

### <span data-ttu-id="1d74d-105">ByAlertId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1d74d-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d74d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d74d-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d74d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1d74d-107">DESCRIPTION</span></span>
<span data-ttu-id="1d74d-108">Polecenie cmdlet **Get-AzAlertObjectHistory** pobiera historię alertu.</span><span class="sxs-lookup"><span data-stu-id="1d74d-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="1d74d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d74d-109">EXAMPLES</span></span>

### <span data-ttu-id="1d74d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d74d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="1d74d-111">Pobiera szczegóły historii alertu.</span><span class="sxs-lookup"><span data-stu-id="1d74d-111">Gets alert history details.</span></span> 

## <span data-ttu-id="1d74d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d74d-112">PARAMETERS</span></span>

### <span data-ttu-id="1d74d-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="1d74d-113">-AlertId</span></span>
<span data-ttu-id="1d74d-114">Unikatowy identyfikator alertu/ResourceId alertu.</span><span class="sxs-lookup"><span data-stu-id="1d74d-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d74d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d74d-115">-DefaultProfile</span></span>
<span data-ttu-id="1d74d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d74d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d74d-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1d74d-117">-InputObject</span></span>
<span data-ttu-id="1d74d-118">Obiekt wejściowy z potoku.</span><span class="sxs-lookup"><span data-stu-id="1d74d-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="1d74d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d74d-119">CommonParameters</span></span>
<span data-ttu-id="1d74d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d74d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d74d-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d74d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d74d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d74d-122">INPUTS</span></span>

### <span data-ttu-id="1d74d-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1d74d-123">None</span></span>

## <span data-ttu-id="1d74d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d74d-124">OUTPUTS</span></span>

### <span data-ttu-id="1d74d-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="1d74d-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="1d74d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d74d-126">NOTES</span></span>

## <span data-ttu-id="1d74d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d74d-127">RELATED LINKS</span></span>
