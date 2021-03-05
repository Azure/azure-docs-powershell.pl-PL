---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1e6f6957adc8a67e1d92c0aad6f2be035b4f390d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963121"
---
# <span data-ttu-id="f60d5-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="f60d5-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="f60d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f60d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f60d5-103">Usuwa określone zasady obliczeniowe usługi Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f60d5-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="f60d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f60d5-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f60d5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f60d5-105">DESCRIPTION</span></span>
<span data-ttu-id="f60d5-106">Ustawienie **Remove-AzDataLakeAnalyticsComputePolicy** usuwa określone zasady obliczeniowe usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f60d5-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="f60d5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f60d5-107">EXAMPLES</span></span>

### <span data-ttu-id="f60d5-108">Przykład 1. Usuwanie zasad obliczania</span><span class="sxs-lookup"><span data-stu-id="f60d5-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="f60d5-109">To polecenie usuwa określone zasady obliczeniowe o nazwie "myPolicy" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="f60d5-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="f60d5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f60d5-110">PARAMETERS</span></span>

### <span data-ttu-id="f60d5-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="f60d5-111">-Account</span></span>
<span data-ttu-id="f60d5-112">Nazwa konta, z których mają być usuwane zasady obliczania.</span><span class="sxs-lookup"><span data-stu-id="f60d5-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="f60d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60d5-113">-DefaultProfile</span></span>
<span data-ttu-id="f60d5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f60d5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f60d5-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f60d5-115">-Name</span></span>
<span data-ttu-id="f60d5-116">Nazwa zasad obliczania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f60d5-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="f60d5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f60d5-117">-PassThru</span></span>
<span data-ttu-id="f60d5-118">Zwróć wartość true po pomyślnym usunięciu.</span><span class="sxs-lookup"><span data-stu-id="f60d5-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="f60d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f60d5-119">-ResourceGroupName</span></span>
<span data-ttu-id="f60d5-120">Nazwa grupy zasobów, w której istnieje konto.</span><span class="sxs-lookup"><span data-stu-id="f60d5-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="f60d5-121">Opcjonalne i podejmie próbę odnajdowania, jeśli nie zostanie podany.</span><span class="sxs-lookup"><span data-stu-id="f60d5-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="f60d5-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f60d5-122">-Confirm</span></span>
<span data-ttu-id="f60d5-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f60d5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f60d5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f60d5-124">-WhatIf</span></span>
<span data-ttu-id="f60d5-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f60d5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f60d5-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f60d5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f60d5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60d5-127">CommonParameters</span></span>
<span data-ttu-id="f60d5-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f60d5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60d5-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f60d5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60d5-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f60d5-130">INPUTS</span></span>

### <span data-ttu-id="f60d5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f60d5-131">System.String</span></span>

## <span data-ttu-id="f60d5-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f60d5-132">OUTPUTS</span></span>

### <span data-ttu-id="f60d5-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f60d5-133">System.Boolean</span></span>

## <span data-ttu-id="f60d5-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f60d5-134">NOTES</span></span>

## <span data-ttu-id="f60d5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f60d5-135">RELATED LINKS</span></span>
