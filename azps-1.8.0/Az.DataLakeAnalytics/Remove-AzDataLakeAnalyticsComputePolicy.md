---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: deafb0cb68ab58997df83bc0280b50a4cc4a0de0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710053"
---
# <span data-ttu-id="380fa-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="380fa-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="380fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="380fa-102">SYNOPSIS</span></span>
<span data-ttu-id="380fa-103">Usuwa określoną zasadę obliczania usługi Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="380fa-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="380fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="380fa-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="380fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="380fa-105">DESCRIPTION</span></span>
<span data-ttu-id="380fa-106">**Element Remove-AzDataLakeAnalyticsComputePolicy** usuwa określoną zasadę obliczeniową usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="380fa-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="380fa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="380fa-107">EXAMPLES</span></span>

### <span data-ttu-id="380fa-108">Przykład 1. Usuń zasady obliczania</span><span class="sxs-lookup"><span data-stu-id="380fa-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="380fa-109">To polecenie usuwa określoną zasadę obliczeniową z nazwą "Moja zasada" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="380fa-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="380fa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="380fa-110">PARAMETERS</span></span>

### <span data-ttu-id="380fa-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="380fa-111">-Account</span></span>
<span data-ttu-id="380fa-112">Nazwa konta, z którego mają zostać usunięte zasady obliczania.</span><span class="sxs-lookup"><span data-stu-id="380fa-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380fa-113">-DefaultProfile</span></span>
<span data-ttu-id="380fa-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="380fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="380fa-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="380fa-115">-Name</span></span>
<span data-ttu-id="380fa-116">Nazwa zasad obliczania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="380fa-116">Name of the compute policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380fa-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="380fa-117">-PassThru</span></span>
<span data-ttu-id="380fa-118">Zwraca wartość Prawda po udanym usunięciu.</span><span class="sxs-lookup"><span data-stu-id="380fa-118">Return true upon successful deletion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380fa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="380fa-119">-ResourceGroupName</span></span>
<span data-ttu-id="380fa-120">Nazwa grupy zasobów, pod którą konto istnieje.</span><span class="sxs-lookup"><span data-stu-id="380fa-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="380fa-121">Opcjonalny i będzie próbować wykryć, czy nie podano.</span><span class="sxs-lookup"><span data-stu-id="380fa-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380fa-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="380fa-122">-Confirm</span></span>
<span data-ttu-id="380fa-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="380fa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="380fa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="380fa-124">-WhatIf</span></span>
<span data-ttu-id="380fa-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="380fa-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="380fa-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="380fa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="380fa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380fa-127">CommonParameters</span></span>
<span data-ttu-id="380fa-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="380fa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380fa-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="380fa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380fa-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="380fa-130">INPUTS</span></span>

### <span data-ttu-id="380fa-131">System. String</span><span class="sxs-lookup"><span data-stu-id="380fa-131">System.String</span></span>

## <span data-ttu-id="380fa-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="380fa-132">OUTPUTS</span></span>

### <span data-ttu-id="380fa-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="380fa-133">System.Boolean</span></span>

## <span data-ttu-id="380fa-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="380fa-134">NOTES</span></span>

## <span data-ttu-id="380fa-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="380fa-135">RELATED LINKS</span></span>
