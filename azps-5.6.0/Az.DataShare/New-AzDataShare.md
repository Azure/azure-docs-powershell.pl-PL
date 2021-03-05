---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: cda809b8c6c4425a3df7bd4ba5ae40a9292e358f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998348"
---
# <span data-ttu-id="8fc77-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="8fc77-101">New-AzDataShare</span></span>

## <span data-ttu-id="8fc77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fc77-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc77-103">Tworzy udział danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8fc77-103">Creates a azure data share.</span></span>

## <span data-ttu-id="8fc77-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8fc77-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fc77-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8fc77-105">DESCRIPTION</span></span>
<span data-ttu-id="8fc77-106">Polecenie **cmdlet New-AzDataShare** tworzy udział danych w określonym koncie udziału danych platformy Azure, podając nazwę grupy zasobów, nazwę konta, nazwę udostępniania i rodzaj udziału.</span><span class="sxs-lookup"><span data-stu-id="8fc77-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="8fc77-107">Opis i warunki użytkowania to opcjonalne parametry, które można ustawiać podczas tworzenia udziału danych.</span><span class="sxs-lookup"><span data-stu-id="8fc77-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="8fc77-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8fc77-108">EXAMPLES</span></span>

### <span data-ttu-id="8fc77-109">Przykład 1. Tworzenie udziału danych</span><span class="sxs-lookup"><span data-stu-id="8fc77-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="8fc77-110">To polecenie umożliwia utworzenie udziału danych o nazwie AdsShare typu CopyBased in data share account WikiAdsAccount w grupie zasobów ADS z opisem i warunkami użytkowania.</span><span class="sxs-lookup"><span data-stu-id="8fc77-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="8fc77-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fc77-111">PARAMETERS</span></span>

### <span data-ttu-id="8fc77-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8fc77-112">-AccountName</span></span>
<span data-ttu-id="8fc77-113">Nazwa konta współużytkowego danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8fc77-113">Azure data share account name</span></span>

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

### <span data-ttu-id="8fc77-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc77-114">-DefaultProfile</span></span>
<span data-ttu-id="8fc77-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8fc77-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fc77-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="8fc77-116">-Description</span></span>
<span data-ttu-id="8fc77-117">Opis udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8fc77-117">Description of azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc77-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8fc77-118">-Name</span></span>
<span data-ttu-id="8fc77-119">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8fc77-119">Azure data share name</span></span>

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

### <span data-ttu-id="8fc77-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc77-120">-ResourceGroupName</span></span>
<span data-ttu-id="8fc77-121">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="8fc77-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8fc77-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="8fc77-122">-TermsOfUse</span></span>
<span data-ttu-id="8fc77-123">Warunki użytkowania dla udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8fc77-123">Terms of use for azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc77-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8fc77-124">-Confirm</span></span>
<span data-ttu-id="8fc77-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8fc77-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc77-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc77-126">-WhatIf</span></span>
<span data-ttu-id="8fc77-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fc77-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc77-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8fc77-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc77-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc77-129">CommonParameters</span></span>
<span data-ttu-id="8fc77-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fc77-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc77-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fc77-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc77-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fc77-132">INPUTS</span></span>

### <span data-ttu-id="8fc77-133">Brak</span><span class="sxs-lookup"><span data-stu-id="8fc77-133">None</span></span>

## <span data-ttu-id="8fc77-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fc77-134">OUTPUTS</span></span>

### <span data-ttu-id="8fc77-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="8fc77-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="8fc77-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8fc77-136">NOTES</span></span>

## <span data-ttu-id="8fc77-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fc77-137">RELATED LINKS</span></span>
