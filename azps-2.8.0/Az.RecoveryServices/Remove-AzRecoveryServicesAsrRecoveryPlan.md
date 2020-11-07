---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4931b32cf2c74180ad06b071d19ef57f4be2285e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872611"
---
# <span data-ttu-id="9ff19-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ff19-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="9ff19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ff19-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff19-103">Usuwa określony plan odzyskiwania ASR z magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="9ff19-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="9ff19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ff19-104">SYNTAX</span></span>

### <span data-ttu-id="9ff19-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ff19-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ff19-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9ff19-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ff19-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9ff19-107">DESCRIPTION</span></span>
<span data-ttu-id="9ff19-108">Polecenie cmdlet **Remove-AzRecoveryServicesAsrRecoveryPlan** usuwa określony plan odzyskiwania z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9ff19-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="9ff19-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ff19-109">EXAMPLES</span></span>

### <span data-ttu-id="9ff19-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ff19-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="9ff19-111">Rozpoczyna usuwanie określonego planu odzyskiwania i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="9ff19-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9ff19-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ff19-112">PARAMETERS</span></span>

### <span data-ttu-id="9ff19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff19-113">-DefaultProfile</span></span>
<span data-ttu-id="9ff19-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff19-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9ff19-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ff19-115">-InputObject</span></span>
<span data-ttu-id="9ff19-116">Obiekt wejściowy do polecenia cmdlet: obiekt planu odzyskiwania ASR odpowiadający planowi odzyskiwania do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9ff19-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff19-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ff19-117">-Name</span></span>
<span data-ttu-id="9ff19-118">Określa nazwę planu odzyskiwania, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="9ff19-118">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff19-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ff19-119">-Confirm</span></span>
<span data-ttu-id="9ff19-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ff19-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ff19-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff19-121">-WhatIf</span></span>
<span data-ttu-id="9ff19-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ff19-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ff19-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ff19-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ff19-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff19-124">CommonParameters</span></span>
<span data-ttu-id="9ff19-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff19-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff19-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff19-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff19-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ff19-127">INPUTS</span></span>

### <span data-ttu-id="9ff19-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ff19-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="9ff19-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ff19-129">OUTPUTS</span></span>

### <span data-ttu-id="9ff19-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9ff19-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9ff19-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ff19-131">NOTES</span></span>

## <span data-ttu-id="9ff19-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ff19-132">RELATED LINKS</span></span>

[<span data-ttu-id="9ff19-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ff19-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9ff19-134">Nowe — AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ff19-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9ff19-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ff19-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


