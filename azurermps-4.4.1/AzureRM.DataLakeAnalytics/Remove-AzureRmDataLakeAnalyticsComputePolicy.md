---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 8be60712f0687edcbd036c48a079e3ecb90ec6c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551067"
---
# <span data-ttu-id="1a73a-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="1a73a-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="1a73a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a73a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a73a-103">Usuwa określoną zasadę obliczania usługi Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="1a73a-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a73a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a73a-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a73a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1a73a-105">DESCRIPTION</span></span>
<span data-ttu-id="1a73a-106">**Element Remove-AzureRmDataLakeAnalyticsComputePolicy** usuwa określoną zasadę obliczeniową usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1a73a-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="1a73a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a73a-107">EXAMPLES</span></span>

### <span data-ttu-id="1a73a-108">Przykład 1. Usuń zasady obliczania</span><span class="sxs-lookup"><span data-stu-id="1a73a-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="1a73a-109">To polecenie usuwa określoną zasadę obliczeniową z nazwą "Moja zasada" na koncie "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="1a73a-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="1a73a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a73a-110">PARAMETERS</span></span>

### <span data-ttu-id="1a73a-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="1a73a-111">-Account</span></span>
<span data-ttu-id="1a73a-112">Nazwa konta, z którego mają zostać usunięte zasady obliczania.</span><span class="sxs-lookup"><span data-stu-id="1a73a-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="1a73a-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a73a-113">-Name</span></span>
<span data-ttu-id="1a73a-114">Nazwa zasad obliczania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1a73a-114">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="1a73a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a73a-115">-PassThru</span></span>
<span data-ttu-id="1a73a-116">Zwraca wartość Prawda po udanym usunięciu.</span><span class="sxs-lookup"><span data-stu-id="1a73a-116">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="1a73a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a73a-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a73a-118">Nazwa grupy zasobów, pod którą konto istnieje.</span><span class="sxs-lookup"><span data-stu-id="1a73a-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="1a73a-119">Opcjonalny i będzie próbować wykryć, czy nie podano.</span><span class="sxs-lookup"><span data-stu-id="1a73a-119">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="1a73a-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a73a-120">-Confirm</span></span>
<span data-ttu-id="1a73a-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a73a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a73a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a73a-122">-WhatIf</span></span>
<span data-ttu-id="1a73a-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a73a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a73a-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1a73a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a73a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a73a-125">-DefaultProfile</span></span>
<span data-ttu-id="1a73a-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a73a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a73a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a73a-127">CommonParameters</span></span>
<span data-ttu-id="1a73a-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a73a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a73a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a73a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a73a-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a73a-130">INPUTS</span></span>

### <span data-ttu-id="1a73a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1a73a-131">System.String</span></span>

## <span data-ttu-id="1a73a-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a73a-132">OUTPUTS</span></span>

### <span data-ttu-id="1a73a-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a73a-133">System.Boolean</span></span>

## <span data-ttu-id="1a73a-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a73a-134">NOTES</span></span>

## <span data-ttu-id="1a73a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a73a-135">RELATED LINKS</span></span>

