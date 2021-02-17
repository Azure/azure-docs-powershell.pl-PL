---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: b60b43b2c0a28be969ad633c80338f42b2c98db6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180835"
---
# <span data-ttu-id="e505a-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="e505a-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="e505a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e505a-102">SYNOPSIS</span></span>
<span data-ttu-id="e505a-103">Pobiera informacje o ustawieniu synchronizacji dla udziału.</span><span class="sxs-lookup"><span data-stu-id="e505a-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="e505a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e505a-104">SYNTAX</span></span>

### <span data-ttu-id="e505a-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e505a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e505a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e505a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e505a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e505a-107">DESCRIPTION</span></span>
<span data-ttu-id="e505a-108">Polecenie **cmdlet Get-AzDataShareSynchronization** dostarcza informacji o wszystkich ustawieniach synchronizacji obecnych w udostępnieniu w ramach konta udziału danych.</span><span class="sxs-lookup"><span data-stu-id="e505a-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="e505a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e505a-109">EXAMPLES</span></span>

### <span data-ttu-id="e505a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e505a-110">Example 1</span></span>
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

<span data-ttu-id="e505a-111">To polecenia zawierają informacje o wszystkich ustawieniach synchronizacji dostępnych w dziel się z usługą AdsShare w dziel się danymi konta WikiAds.</span><span class="sxs-lookup"><span data-stu-id="e505a-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="e505a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e505a-112">PARAMETERS</span></span>

### <span data-ttu-id="e505a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e505a-113">-AccountName</span></span>
<span data-ttu-id="e505a-114">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e505a-114">Azure data share account name</span></span>

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

### <span data-ttu-id="e505a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e505a-115">-DefaultProfile</span></span>
<span data-ttu-id="e505a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e505a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e505a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e505a-117">-ResourceGroupName</span></span>
<span data-ttu-id="e505a-118">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="e505a-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="e505a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e505a-119">-ResourceId</span></span>
<span data-ttu-id="e505a-120">Identyfikator zasobu współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e505a-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="e505a-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e505a-121">-ShareName</span></span>
<span data-ttu-id="e505a-122">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e505a-122">Azure data share name</span></span>

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

### <span data-ttu-id="e505a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e505a-123">CommonParameters</span></span>
<span data-ttu-id="e505a-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e505a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e505a-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e505a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e505a-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e505a-126">INPUTS</span></span>

### <span data-ttu-id="e505a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e505a-127">System.String</span></span>

## <span data-ttu-id="e505a-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e505a-128">OUTPUTS</span></span>

### <span data-ttu-id="e505a-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="e505a-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="e505a-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e505a-130">NOTES</span></span>

## <span data-ttu-id="e505a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e505a-131">RELATED LINKS</span></span>
