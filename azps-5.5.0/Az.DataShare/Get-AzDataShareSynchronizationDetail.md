---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 2ee3714895b751223768ac3f98efbd04405ae69f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194587"
---
# <span data-ttu-id="3a35a-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="3a35a-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="3a35a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a35a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a35a-103">Pobiera informacje o szczegółach synchronizacji dla udziału.</span><span class="sxs-lookup"><span data-stu-id="3a35a-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="3a35a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3a35a-104">SYNTAX</span></span>

### <span data-ttu-id="3a35a-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3a35a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a35a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a35a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a35a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3a35a-107">DESCRIPTION</span></span>
<span data-ttu-id="3a35a-108">Polecenie **cmdlet Get-AzDataShareSynchronizationDetail** zawiera szczegóły synchronizacji zainicjowanej dla udziału.</span><span class="sxs-lookup"><span data-stu-id="3a35a-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="3a35a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3a35a-109">EXAMPLES</span></span>

### <span data-ttu-id="3a35a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a35a-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -SynchronizationId "02a17faa-4498-45ee-a884-162180af9251"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="3a35a-111">To polecenie zawiera informacje o szczegółach synchronizacji wszystkich zestawów danych odpowiadających podanego identyfikatora synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="3a35a-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="3a35a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a35a-112">PARAMETERS</span></span>

### <span data-ttu-id="3a35a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3a35a-113">-AccountName</span></span>
<span data-ttu-id="3a35a-114">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3a35a-114">Azure data share account name</span></span>

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

### <span data-ttu-id="3a35a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a35a-115">-DefaultProfile</span></span>
<span data-ttu-id="3a35a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a35a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a35a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a35a-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a35a-118">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3a35a-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3a35a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a35a-119">-ResourceId</span></span>
<span data-ttu-id="3a35a-120">Identyfikator zasobu współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3a35a-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="3a35a-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3a35a-121">-ShareName</span></span>
<span data-ttu-id="3a35a-122">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3a35a-122">Azure data share name</span></span>

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

### <span data-ttu-id="3a35a-123">- SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="3a35a-123">-SynchronizationId</span></span>
<span data-ttu-id="3a35a-124">Identyfikator synchronizacji synchronizacji udostępniania</span><span class="sxs-lookup"><span data-stu-id="3a35a-124">Synchronization id of share synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a35a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a35a-125">CommonParameters</span></span>
<span data-ttu-id="3a35a-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a35a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a35a-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a35a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a35a-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a35a-128">INPUTS</span></span>

### <span data-ttu-id="3a35a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3a35a-129">System.String</span></span>

## <span data-ttu-id="3a35a-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a35a-130">OUTPUTS</span></span>

### <span data-ttu-id="3a35a-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="3a35a-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="3a35a-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3a35a-132">NOTES</span></span>

## <span data-ttu-id="3a35a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a35a-133">RELATED LINKS</span></span>
