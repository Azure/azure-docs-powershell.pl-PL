---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 5f4298c2a4bfdc081447e6a8b15bac565b20b2db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544228"
---
# <span data-ttu-id="49ed5-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49ed5-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="49ed5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="49ed5-103">Usuwa określony plan odzyskiwania ASR z magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="49ed5-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49ed5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49ed5-104">SYNTAX</span></span>

### <span data-ttu-id="49ed5-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="49ed5-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ed5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="49ed5-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ed5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="49ed5-107">DESCRIPTION</span></span>
<span data-ttu-id="49ed5-108">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** usuwa określony plan odzyskiwania z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="49ed5-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="49ed5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49ed5-109">EXAMPLES</span></span>

### <span data-ttu-id="49ed5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="49ed5-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="49ed5-111">Rozpoczyna usuwanie określonego planu odzyskiwania i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="49ed5-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="49ed5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49ed5-112">PARAMETERS</span></span>

### <span data-ttu-id="49ed5-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49ed5-113">-Confirm</span></span>
<span data-ttu-id="49ed5-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ed5-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ed5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ed5-115">-DefaultProfile</span></span>
<span data-ttu-id="49ed5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49ed5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ed5-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="49ed5-117">-InputObject</span></span>
<span data-ttu-id="49ed5-118">Obiekt wejściowy do polecenia cmdlet: obiekt planu odzyskiwania ASR odpowiadający planowi odzyskiwania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="49ed5-118">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ed5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="49ed5-119">-Name</span></span>
<span data-ttu-id="49ed5-120">Określa nazwę planu odzyskiwania, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="49ed5-120">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ed5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ed5-121">-WhatIf</span></span>
<span data-ttu-id="49ed5-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ed5-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49ed5-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49ed5-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ed5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ed5-124">CommonParameters</span></span>
<span data-ttu-id="49ed5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ed5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ed5-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ed5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ed5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49ed5-127">INPUTS</span></span>

### <span data-ttu-id="49ed5-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49ed5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="49ed5-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49ed5-129">OUTPUTS</span></span>

### <span data-ttu-id="49ed5-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="49ed5-130">System.Object</span></span>

## <span data-ttu-id="49ed5-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49ed5-131">NOTES</span></span>

## <span data-ttu-id="49ed5-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49ed5-132">RELATED LINKS</span></span>

[<span data-ttu-id="49ed5-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49ed5-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="49ed5-134">Nowe — AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49ed5-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="49ed5-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49ed5-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


