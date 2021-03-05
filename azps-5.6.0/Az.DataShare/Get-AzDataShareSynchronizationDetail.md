---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 049b337c1f200115fe1328c70c1f9f7b04c9540f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006794"
---
# <span data-ttu-id="2709c-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="2709c-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="2709c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2709c-102">SYNOPSIS</span></span>
<span data-ttu-id="2709c-103">Pobiera informacje o szczegółach synchronizacji dla udziału.</span><span class="sxs-lookup"><span data-stu-id="2709c-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="2709c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2709c-104">SYNTAX</span></span>

### <span data-ttu-id="2709c-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2709c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2709c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2709c-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2709c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2709c-107">DESCRIPTION</span></span>
<span data-ttu-id="2709c-108">Polecenie **cmdlet Get-AzDataShareSynchronizationDetail** zawiera szczegóły synchronizacji zainicjowanej dla udziału.</span><span class="sxs-lookup"><span data-stu-id="2709c-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="2709c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2709c-109">EXAMPLES</span></span>

### <span data-ttu-id="2709c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2709c-110">Example 1</span></span>
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

<span data-ttu-id="2709c-111">To polecenie zawiera informacje o szczegółach synchronizacji wszystkich zestawów danych odpowiadających podanego identyfikatora synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="2709c-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="2709c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2709c-112">PARAMETERS</span></span>

### <span data-ttu-id="2709c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2709c-113">-AccountName</span></span>
<span data-ttu-id="2709c-114">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2709c-114">Azure data share account name</span></span>

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

### <span data-ttu-id="2709c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2709c-115">-DefaultProfile</span></span>
<span data-ttu-id="2709c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2709c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2709c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2709c-117">-ResourceGroupName</span></span>
<span data-ttu-id="2709c-118">Nazwa grupy zasobów konta udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2709c-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2709c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2709c-119">-ResourceId</span></span>
<span data-ttu-id="2709c-120">Identyfikator zasobu współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2709c-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="2709c-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2709c-121">-ShareName</span></span>
<span data-ttu-id="2709c-122">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2709c-122">Azure data share name</span></span>

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

### <span data-ttu-id="2709c-123">- SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="2709c-123">-SynchronizationId</span></span>
<span data-ttu-id="2709c-124">Identyfikator synchronizacji synchronizacji udostępniania</span><span class="sxs-lookup"><span data-stu-id="2709c-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="2709c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2709c-125">CommonParameters</span></span>
<span data-ttu-id="2709c-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2709c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2709c-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2709c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2709c-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2709c-128">INPUTS</span></span>

### <span data-ttu-id="2709c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2709c-129">System.String</span></span>

## <span data-ttu-id="2709c-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2709c-130">OUTPUTS</span></span>

### <span data-ttu-id="2709c-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="2709c-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="2709c-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2709c-132">NOTES</span></span>

## <span data-ttu-id="2709c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2709c-133">RELATED LINKS</span></span>
