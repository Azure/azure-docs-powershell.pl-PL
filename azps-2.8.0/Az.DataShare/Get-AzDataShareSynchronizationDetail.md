---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: c3320c4b60a91c8a4f4b5c02ab46eb68b2f2d37c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705688"
---
# <span data-ttu-id="f9db3-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="f9db3-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="f9db3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9db3-102">SYNOPSIS</span></span>
<span data-ttu-id="f9db3-103">Pobiera informacje o szczegółach synchronizacji udziału.</span><span class="sxs-lookup"><span data-stu-id="f9db3-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="f9db3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9db3-104">SYNTAX</span></span>

### <span data-ttu-id="f9db3-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f9db3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9db3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9db3-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9db3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f9db3-107">DESCRIPTION</span></span>
<span data-ttu-id="f9db3-108">Polecenie cmdlet **Get-AzDataShareSynchronizationDetail** zawiera szczegółowe informacje dotyczące synchronizacji zainicjowanej dla udziału.</span><span class="sxs-lookup"><span data-stu-id="f9db3-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="f9db3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9db3-109">EXAMPLES</span></span>

### <span data-ttu-id="f9db3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9db3-110">Example 1</span></span>
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

<span data-ttu-id="f9db3-111">To polecenie zawiera informacje o szczegółach synchronizacji wszystkich zestawów danych odpowiadających danemu identyfikatorowi synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="f9db3-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="f9db3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9db3-112">PARAMETERS</span></span>

### <span data-ttu-id="f9db3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f9db3-113">-AccountName</span></span>
<span data-ttu-id="f9db3-114">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="f9db3-114">Azure data share account name</span></span>

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

### <span data-ttu-id="f9db3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9db3-115">-DefaultProfile</span></span>
<span data-ttu-id="f9db3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9db3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9db3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9db3-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9db3-118">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="f9db3-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f9db3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9db3-119">-ResourceId</span></span>
<span data-ttu-id="f9db3-120">Identyfikator zasobu udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="f9db3-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="f9db3-121">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="f9db3-121">-ShareName</span></span>
<span data-ttu-id="f9db3-122">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f9db3-122">Azure data share name</span></span>

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

### <span data-ttu-id="f9db3-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="f9db3-123">-SynchronizationId</span></span>
<span data-ttu-id="f9db3-124">Identyfikator synchronizacji synchronizacji udziału</span><span class="sxs-lookup"><span data-stu-id="f9db3-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="f9db3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9db3-125">CommonParameters</span></span>
<span data-ttu-id="f9db3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9db3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9db3-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9db3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9db3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9db3-128">INPUTS</span></span>

### <span data-ttu-id="f9db3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f9db3-129">System.String</span></span>

## <span data-ttu-id="f9db3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9db3-130">OUTPUTS</span></span>

### <span data-ttu-id="f9db3-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="f9db3-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="f9db3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9db3-132">NOTES</span></span>

## <span data-ttu-id="f9db3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9db3-133">RELATED LINKS</span></span>
