---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: 265f917068237fee13f77eb8c87e0adf8cd12f08
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222614"
---
# <span data-ttu-id="bf529-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="bf529-101">New-AzDataShare</span></span>

## <span data-ttu-id="bf529-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf529-102">SYNOPSIS</span></span>
<span data-ttu-id="bf529-103">Umożliwia utworzenie udziału danych usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="bf529-103">Creates a azure data share.</span></span>

## <span data-ttu-id="bf529-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf529-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf529-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf529-105">DESCRIPTION</span></span>
<span data-ttu-id="bf529-106">Polecenie cmdlet **New-AzDataShare** tworzy udział danych w określonym koncie usługi Azure Data Share, dostarczając nazwę grupy zasobów, nazwę konta, nazwę udziału i rodzaj udziału.</span><span class="sxs-lookup"><span data-stu-id="bf529-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="bf529-107">Opis i regulamin użytkowania to parametry opcjonalne, które można ustawić podczas tworzenia udziału danych.</span><span class="sxs-lookup"><span data-stu-id="bf529-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="bf529-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf529-108">EXAMPLES</span></span>

### <span data-ttu-id="bf529-109">Przykład 1. Tworzenie udziału danych</span><span class="sxs-lookup"><span data-stu-id="bf529-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="bf529-110">To polecenie tworzy udział danych o nazwie AdsShare dla CopyBased w koncie udziału danych WikiAdsAccount w obszarze reklamy grup zasobów z opisem i warunkami użytkowania.</span><span class="sxs-lookup"><span data-stu-id="bf529-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="bf529-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf529-111">PARAMETERS</span></span>

### <span data-ttu-id="bf529-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf529-112">-AccountName</span></span>
<span data-ttu-id="bf529-113">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="bf529-113">Azure data share account name</span></span>

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

### <span data-ttu-id="bf529-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf529-114">-DefaultProfile</span></span>
<span data-ttu-id="bf529-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf529-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf529-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="bf529-116">-Description</span></span>
<span data-ttu-id="bf529-117">Opis usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="bf529-117">Description of azure data share</span></span>

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

### <span data-ttu-id="bf529-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf529-118">-Name</span></span>
<span data-ttu-id="bf529-119">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bf529-119">Azure data share name</span></span>

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

### <span data-ttu-id="bf529-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf529-120">-ResourceGroupName</span></span>
<span data-ttu-id="bf529-121">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="bf529-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="bf529-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="bf529-122">-TermsOfUse</span></span>
<span data-ttu-id="bf529-123">Warunki użytkowania usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="bf529-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="bf529-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf529-124">-Confirm</span></span>
<span data-ttu-id="bf529-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf529-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf529-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf529-126">-WhatIf</span></span>
<span data-ttu-id="bf529-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf529-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf529-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf529-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf529-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf529-129">CommonParameters</span></span>
<span data-ttu-id="bf529-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf529-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf529-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf529-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf529-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf529-132">INPUTS</span></span>

### <span data-ttu-id="bf529-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bf529-133">None</span></span>

## <span data-ttu-id="bf529-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf529-134">OUTPUTS</span></span>

### <span data-ttu-id="bf529-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="bf529-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="bf529-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf529-136">NOTES</span></span>

## <span data-ttu-id="bf529-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf529-137">RELATED LINKS</span></span>
