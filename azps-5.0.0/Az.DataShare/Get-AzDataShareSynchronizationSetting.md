---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305233"
---
# <span data-ttu-id="652a1-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="652a1-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="652a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="652a1-102">SYNOPSIS</span></span>
<span data-ttu-id="652a1-103">Pobiera informacje o ustawieniu synchronizacji w udziale.</span><span class="sxs-lookup"><span data-stu-id="652a1-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="652a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="652a1-104">SYNTAX</span></span>

### <span data-ttu-id="652a1-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="652a1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="652a1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="652a1-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="652a1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="652a1-107">DESCRIPTION</span></span>
<span data-ttu-id="652a1-108">Polecenie cmdlet **Get-AzDataShareSynchronizationSetting** zawiera informacje dotyczące synchronizacji włączone w udziale.</span><span class="sxs-lookup"><span data-stu-id="652a1-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="652a1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="652a1-109">EXAMPLES</span></span>

### <span data-ttu-id="652a1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="652a1-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="652a1-111">To polecenie udostępnia informacje na temat ShareSynchronization synchronizacji włączonej AdsShare w obszarze konto udziału danych WikiAds.</span><span class="sxs-lookup"><span data-stu-id="652a1-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="652a1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="652a1-112">PARAMETERS</span></span>

### <span data-ttu-id="652a1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="652a1-113">-AccountName</span></span>
<span data-ttu-id="652a1-114">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="652a1-114">Azure data share account name</span></span>

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

### <span data-ttu-id="652a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="652a1-115">-DefaultProfile</span></span>
<span data-ttu-id="652a1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="652a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="652a1-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="652a1-117">-Name</span></span>
<span data-ttu-id="652a1-118">Nazwa ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="652a1-118">Name for Synchronization Setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="652a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="652a1-120">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="652a1-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="652a1-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="652a1-121">-ResourceId</span></span>
<span data-ttu-id="652a1-122">Identyfikator zasobu Ustawienia synchronizacji udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="652a1-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="652a1-123">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="652a1-123">-ShareName</span></span>
<span data-ttu-id="652a1-124">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="652a1-124">Azure data share name</span></span>

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

### <span data-ttu-id="652a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="652a1-125">CommonParameters</span></span>
<span data-ttu-id="652a1-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="652a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="652a1-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="652a1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="652a1-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="652a1-128">INPUTS</span></span>

### <span data-ttu-id="652a1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="652a1-129">System.String</span></span>

## <span data-ttu-id="652a1-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="652a1-130">OUTPUTS</span></span>

### <span data-ttu-id="652a1-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="652a1-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="652a1-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="652a1-132">NOTES</span></span>

## <span data-ttu-id="652a1-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="652a1-133">RELATED LINKS</span></span>
