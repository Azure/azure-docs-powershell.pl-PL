---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 55e887ed60eaf4dd4fc6c26423686b99572702ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006785"
---
# <span data-ttu-id="5a463-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="5a463-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="5a463-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a463-102">SYNOPSIS</span></span>
<span data-ttu-id="5a463-103">Pobiera informacje o ustawieniu synchronizacji dla udziału.</span><span class="sxs-lookup"><span data-stu-id="5a463-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="5a463-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a463-104">SYNTAX</span></span>

### <span data-ttu-id="5a463-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5a463-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a463-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a463-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a463-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a463-107">DESCRIPTION</span></span>
<span data-ttu-id="5a463-108">Polecenie **cmdlet Get-AzDataShareSynchronizationSetting** udostępnia informacje o synchronizacji włączonej w udostępnieniu.</span><span class="sxs-lookup"><span data-stu-id="5a463-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="5a463-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a463-109">EXAMPLES</span></span>

### <span data-ttu-id="5a463-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5a463-110">Example 1</span></span>
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

<span data-ttu-id="5a463-111">To polecenie zawiera informacje na temat synchronizacji włączonej synchronizacji synchronizacji usługi ShareSynchronization w dzieleniu usługi AdsShare w obszarze WikiAds konta udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="5a463-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="5a463-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a463-112">PARAMETERS</span></span>

### <span data-ttu-id="5a463-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5a463-113">-AccountName</span></span>
<span data-ttu-id="5a463-114">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5a463-114">Azure data share account name</span></span>

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

### <span data-ttu-id="5a463-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a463-115">-DefaultProfile</span></span>
<span data-ttu-id="5a463-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a463-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a463-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5a463-117">-Name</span></span>
<span data-ttu-id="5a463-118">Nazwa ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="5a463-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="5a463-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a463-119">-ResourceGroupName</span></span>
<span data-ttu-id="5a463-120">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="5a463-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="5a463-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a463-121">-ResourceId</span></span>
<span data-ttu-id="5a463-122">Identyfikator zasobu ustawienia synchronizacji udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5a463-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="5a463-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="5a463-123">-ShareName</span></span>
<span data-ttu-id="5a463-124">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5a463-124">Azure data share name</span></span>

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

### <span data-ttu-id="5a463-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a463-125">CommonParameters</span></span>
<span data-ttu-id="5a463-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a463-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a463-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a463-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a463-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a463-128">INPUTS</span></span>

### <span data-ttu-id="5a463-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5a463-129">System.String</span></span>

## <span data-ttu-id="5a463-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a463-130">OUTPUTS</span></span>

### <span data-ttu-id="5a463-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="5a463-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="5a463-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a463-132">NOTES</span></span>

## <span data-ttu-id="5a463-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a463-133">RELATED LINKS</span></span>
