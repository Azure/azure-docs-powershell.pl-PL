---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: 8c0df920b8619760cf4a80d9ef6502e82de9a31f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707154"
---
# <span data-ttu-id="b8f37-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="b8f37-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="b8f37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8f37-102">SYNOPSIS</span></span>
<span data-ttu-id="b8f37-103">Pobiera informacje o historii alertu</span><span class="sxs-lookup"><span data-stu-id="b8f37-103">Gets Alert History information</span></span>

## <span data-ttu-id="b8f37-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8f37-104">SYNTAX</span></span>

### <span data-ttu-id="b8f37-105">ByAlertId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b8f37-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8f37-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b8f37-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8f37-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b8f37-107">DESCRIPTION</span></span>
<span data-ttu-id="b8f37-108">Polecenie cmdlet **Get-AzAlertObjectHistory** pobiera historię alertu.</span><span class="sxs-lookup"><span data-stu-id="b8f37-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="b8f37-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8f37-109">EXAMPLES</span></span>

### <span data-ttu-id="b8f37-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8f37-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="b8f37-111">Pobiera szczegóły historii alertu.</span><span class="sxs-lookup"><span data-stu-id="b8f37-111">Gets alert history details.</span></span> 

## <span data-ttu-id="b8f37-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8f37-112">PARAMETERS</span></span>

### <span data-ttu-id="b8f37-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="b8f37-113">-AlertId</span></span>
<span data-ttu-id="b8f37-114">Unikatowy identyfikator alertu/ResourceId alertu.</span><span class="sxs-lookup"><span data-stu-id="b8f37-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="b8f37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8f37-115">-DefaultProfile</span></span>
<span data-ttu-id="b8f37-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8f37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8f37-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b8f37-117">-InputObject</span></span>
<span data-ttu-id="b8f37-118">Obiekt wejściowy z potoku.</span><span class="sxs-lookup"><span data-stu-id="b8f37-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="b8f37-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f37-119">CommonParameters</span></span>
<span data-ttu-id="b8f37-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8f37-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f37-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8f37-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f37-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8f37-122">INPUTS</span></span>

### <span data-ttu-id="b8f37-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b8f37-123">None</span></span>

## <span data-ttu-id="b8f37-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8f37-124">OUTPUTS</span></span>

### <span data-ttu-id="b8f37-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="b8f37-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="b8f37-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8f37-126">NOTES</span></span>

## <span data-ttu-id="b8f37-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8f37-127">RELATED LINKS</span></span>
