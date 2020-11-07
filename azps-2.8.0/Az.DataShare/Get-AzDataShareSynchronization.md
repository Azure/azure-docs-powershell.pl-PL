---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: f211579d98957f48a389ad10c6044c6193ad9993
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705689"
---
# <span data-ttu-id="87995-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="87995-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="87995-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87995-102">SYNOPSIS</span></span>
<span data-ttu-id="87995-103">Pobiera informacje o ustawieniu synchronizacji dla udziału.</span><span class="sxs-lookup"><span data-stu-id="87995-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="87995-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87995-104">SYNTAX</span></span>

### <span data-ttu-id="87995-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="87995-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87995-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87995-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87995-107">Opis</span><span class="sxs-lookup"><span data-stu-id="87995-107">DESCRIPTION</span></span>
<span data-ttu-id="87995-108">Polecenie cmdlet **Get-AzDataShareSynchronization** zawiera informacje na temat wszystkich ustawień synchronizacji obecnych w udziale w ramach konta udziału danych.</span><span class="sxs-lookup"><span data-stu-id="87995-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="87995-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87995-109">EXAMPLES</span></span>

### <span data-ttu-id="87995-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87995-110">Example 1</span></span>
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

<span data-ttu-id="87995-111">Te polecenia dostarczają informacji na temat wszystkich ustawień synchronizacji obecnych w artykule udostępnianie AdsShare w WikiAds kont udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="87995-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="87995-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87995-112">PARAMETERS</span></span>

### <span data-ttu-id="87995-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="87995-113">-AccountName</span></span>
<span data-ttu-id="87995-114">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="87995-114">Azure data share account name</span></span>

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

### <span data-ttu-id="87995-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87995-115">-DefaultProfile</span></span>
<span data-ttu-id="87995-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87995-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87995-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87995-117">-ResourceGroupName</span></span>
<span data-ttu-id="87995-118">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="87995-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="87995-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87995-119">-ResourceId</span></span>
<span data-ttu-id="87995-120">Identyfikator zasobu udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="87995-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="87995-121">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="87995-121">-ShareName</span></span>
<span data-ttu-id="87995-122">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="87995-122">Azure data share name</span></span>

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

### <span data-ttu-id="87995-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87995-123">CommonParameters</span></span>
<span data-ttu-id="87995-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87995-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87995-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87995-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87995-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87995-126">INPUTS</span></span>

### <span data-ttu-id="87995-127">System. String</span><span class="sxs-lookup"><span data-stu-id="87995-127">System.String</span></span>

## <span data-ttu-id="87995-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87995-128">OUTPUTS</span></span>

### <span data-ttu-id="87995-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="87995-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="87995-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87995-130">NOTES</span></span>

## <span data-ttu-id="87995-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87995-131">RELATED LINKS</span></span>
