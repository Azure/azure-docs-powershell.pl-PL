---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: a4d3adbcc63eda80bced31523a43cbbad4513205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990298"
---
# <span data-ttu-id="f0bc0-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="f0bc0-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="f0bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="f0bc0-103">Pobiera informacje o ustawieniu synchronizacji dla udziału.</span><span class="sxs-lookup"><span data-stu-id="f0bc0-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="f0bc0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f0bc0-104">SYNTAX</span></span>

### <span data-ttu-id="f0bc0-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f0bc0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0bc0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0bc0-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0bc0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f0bc0-107">DESCRIPTION</span></span>
<span data-ttu-id="f0bc0-108">Polecenie **cmdlet Get-AzDataShareSynchronization** dostarcza informacji o wszystkich ustawieniach synchronizacji obecnych w udostępnieniu w ramach konta udziału danych.</span><span class="sxs-lookup"><span data-stu-id="f0bc0-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="f0bc0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f0bc0-109">EXAMPLES</span></span>

### <span data-ttu-id="f0bc0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f0bc0-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="f0bc0-111">To polecenia zawierają informacje o wszystkich ustawieniach synchronizacji dostępnych w dzielenia usługi AdsShare w dziel się danymi konta WikiAds.</span><span class="sxs-lookup"><span data-stu-id="f0bc0-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="f0bc0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0bc0-112">PARAMETERS</span></span>

### <span data-ttu-id="f0bc0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f0bc0-113">-AccountName</span></span>
<span data-ttu-id="f0bc0-114">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f0bc0-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bc0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0bc0-115">-DefaultProfile</span></span>
<span data-ttu-id="f0bc0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0bc0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0bc0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0bc0-117">-ResourceGroupName</span></span>
<span data-ttu-id="f0bc0-118">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f0bc0-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bc0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0bc0-119">-ResourceId</span></span>
<span data-ttu-id="f0bc0-120">Identyfikator zasobu współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f0bc0-120">Azure data share resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0bc0-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f0bc0-121">-ShareName</span></span>
<span data-ttu-id="f0bc0-122">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f0bc0-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0bc0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0bc0-123">CommonParameters</span></span>
<span data-ttu-id="f0bc0-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0bc0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0bc0-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0bc0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0bc0-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0bc0-126">INPUTS</span></span>

### <span data-ttu-id="f0bc0-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f0bc0-127">System.String</span></span>

## <span data-ttu-id="f0bc0-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0bc0-128">OUTPUTS</span></span>

### <span data-ttu-id="f0bc0-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="f0bc0-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="f0bc0-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f0bc0-130">NOTES</span></span>

## <span data-ttu-id="f0bc0-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0bc0-131">RELATED LINKS</span></span>
