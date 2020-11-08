---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: c92348e32247bfed0b3aa7ce59b4772f7d3ef4af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053383"
---
# <span data-ttu-id="08986-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="08986-101">Set-AzDataShare</span></span>

## <span data-ttu-id="08986-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08986-102">SYNOPSIS</span></span>
<span data-ttu-id="08986-103">Aktualizuje istniejący udział danych</span><span class="sxs-lookup"><span data-stu-id="08986-103">Updates an existing data share</span></span>

## <span data-ttu-id="08986-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08986-104">SYNTAX</span></span>

### <span data-ttu-id="08986-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="08986-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08986-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08986-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08986-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08986-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08986-108">Opis</span><span class="sxs-lookup"><span data-stu-id="08986-108">DESCRIPTION</span></span>
<span data-ttu-id="08986-109">Polecenie cmdlet **Set-AzDataShare** aktualizuje udział danych istniejący w określonym koncie usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="08986-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="08986-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08986-110">EXAMPLES</span></span>

### <span data-ttu-id="08986-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="08986-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="08986-112">To polecenie aktualizuje istniejący udział danych o nazwie AdsShare</span><span class="sxs-lookup"><span data-stu-id="08986-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="08986-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08986-113">PARAMETERS</span></span>

### <span data-ttu-id="08986-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="08986-114">-AccountName</span></span>
<span data-ttu-id="08986-115">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="08986-115">Azure data share account name</span></span>

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

### <span data-ttu-id="08986-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08986-116">-DefaultProfile</span></span>
<span data-ttu-id="08986-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08986-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08986-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="08986-118">-Description</span></span>
<span data-ttu-id="08986-119">Opis udziału danych</span><span class="sxs-lookup"><span data-stu-id="08986-119">Description of Data Share</span></span>

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

### <span data-ttu-id="08986-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="08986-120">-InputObject</span></span>
<span data-ttu-id="08986-121">Obiekt udostępniania danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="08986-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08986-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08986-122">-Name</span></span>
<span data-ttu-id="08986-123">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="08986-123">Azure data share name</span></span>

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

### <span data-ttu-id="08986-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08986-124">-ResourceGroupName</span></span>
<span data-ttu-id="08986-125">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="08986-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="08986-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08986-126">-ResourceId</span></span>
<span data-ttu-id="08986-127">Identyfikator zasobu udziału danych usługi Azure</span><span class="sxs-lookup"><span data-stu-id="08986-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="08986-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="08986-128">-TermsOfUse</span></span>
<span data-ttu-id="08986-129">Warunki użytkowania udostępniania danych</span><span class="sxs-lookup"><span data-stu-id="08986-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="08986-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08986-130">-Confirm</span></span>
<span data-ttu-id="08986-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08986-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08986-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08986-132">-WhatIf</span></span>
<span data-ttu-id="08986-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08986-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08986-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08986-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08986-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08986-135">CommonParameters</span></span>
<span data-ttu-id="08986-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08986-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08986-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08986-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08986-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08986-138">INPUTS</span></span>

### <span data-ttu-id="08986-139">System. String</span><span class="sxs-lookup"><span data-stu-id="08986-139">System.String</span></span>

### <span data-ttu-id="08986-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="08986-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="08986-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08986-141">OUTPUTS</span></span>

### <span data-ttu-id="08986-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="08986-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="08986-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08986-143">NOTES</span></span>

## <span data-ttu-id="08986-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08986-144">RELATED LINKS</span></span>
