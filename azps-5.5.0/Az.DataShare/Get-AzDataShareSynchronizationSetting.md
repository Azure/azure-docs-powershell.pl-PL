---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180827"
---
# <span data-ttu-id="043a5-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="043a5-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="043a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="043a5-102">SYNOPSIS</span></span>
<span data-ttu-id="043a5-103">Pobiera informacje o ustawieniu synchronizacji dla udziału.</span><span class="sxs-lookup"><span data-stu-id="043a5-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="043a5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="043a5-104">SYNTAX</span></span>

### <span data-ttu-id="043a5-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="043a5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="043a5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="043a5-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="043a5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="043a5-107">DESCRIPTION</span></span>
<span data-ttu-id="043a5-108">Polecenie **cmdlet Get-AzDataShareSynchronizationSetting** udostępnia informacje o synchronizacji włączonej w udostępnieniu.</span><span class="sxs-lookup"><span data-stu-id="043a5-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="043a5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="043a5-109">EXAMPLES</span></span>

### <span data-ttu-id="043a5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="043a5-110">Example 1</span></span>
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

<span data-ttu-id="043a5-111">To polecenie zawiera informacje na temat synchronizacji włączonej synchronizacji synchronizacji usługi ShareSynchronization w dzieleniu usługi AdsShare w obszarze WikiAds konta udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="043a5-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="043a5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="043a5-112">PARAMETERS</span></span>

### <span data-ttu-id="043a5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="043a5-113">-AccountName</span></span>
<span data-ttu-id="043a5-114">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="043a5-114">Azure data share account name</span></span>

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

### <span data-ttu-id="043a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="043a5-115">-DefaultProfile</span></span>
<span data-ttu-id="043a5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="043a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="043a5-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="043a5-117">-Name</span></span>
<span data-ttu-id="043a5-118">Nazwa ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="043a5-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="043a5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="043a5-119">-ResourceGroupName</span></span>
<span data-ttu-id="043a5-120">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="043a5-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="043a5-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="043a5-121">-ResourceId</span></span>
<span data-ttu-id="043a5-122">Identyfikator zasobu ustawienia synchronizacji udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="043a5-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="043a5-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="043a5-123">-ShareName</span></span>
<span data-ttu-id="043a5-124">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="043a5-124">Azure data share name</span></span>

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

### <span data-ttu-id="043a5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043a5-125">CommonParameters</span></span>
<span data-ttu-id="043a5-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="043a5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043a5-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="043a5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043a5-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="043a5-128">INPUTS</span></span>

### <span data-ttu-id="043a5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="043a5-129">System.String</span></span>

## <span data-ttu-id="043a5-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="043a5-130">OUTPUTS</span></span>

### <span data-ttu-id="043a5-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="043a5-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="043a5-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="043a5-132">NOTES</span></span>

## <span data-ttu-id="043a5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="043a5-133">RELATED LINKS</span></span>
