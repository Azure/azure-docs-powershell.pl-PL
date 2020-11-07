---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 9a67729b384703ccc102b14d521d4422825bdb6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886669"
---
# <span data-ttu-id="9b716-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="9b716-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="9b716-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b716-102">SYNOPSIS</span></span>
<span data-ttu-id="9b716-103">Usuwa określoną sieć szkieletową odzyskiwania witryny platformy Azure z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9b716-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="9b716-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b716-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b716-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9b716-105">DESCRIPTION</span></span>
<span data-ttu-id="9b716-106">Polecenie cmdlet **Remove-AzRecoveryServicesAsrFabric** usuwa określoną sieć szkieletową odzyskiwania witryny platformy Azure z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="9b716-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="9b716-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b716-107">EXAMPLES</span></span>

### <span data-ttu-id="9b716-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b716-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="9b716-109">Rozpoczyna usuwanie określonej sieci szkieletowej i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="9b716-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9b716-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b716-110">PARAMETERS</span></span>

### <span data-ttu-id="9b716-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b716-111">-DefaultProfile</span></span>
<span data-ttu-id="9b716-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b716-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9b716-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9b716-113">-Force</span></span>
<span data-ttu-id="9b716-114">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="9b716-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="9b716-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b716-115">-InputObject</span></span>
<span data-ttu-id="9b716-116">Obiekt wejściowy do polecenia cmdlet: obiekt sieci szkieletowej ASR odpowiadający sieci szkieletowej, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="9b716-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b716-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b716-117">-Confirm</span></span>
<span data-ttu-id="9b716-118">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="9b716-118">Specify if confirmation is required.</span></span> <span data-ttu-id="9b716-119">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9b716-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="9b716-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b716-120">-WhatIf</span></span>
<span data-ttu-id="9b716-121">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b716-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="9b716-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b716-122">CommonParameters</span></span>
<span data-ttu-id="9b716-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b716-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b716-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b716-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b716-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b716-125">INPUTS</span></span>

### <span data-ttu-id="9b716-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="9b716-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="9b716-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b716-127">OUTPUTS</span></span>

### <span data-ttu-id="9b716-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9b716-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9b716-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b716-129">NOTES</span></span>

## <span data-ttu-id="9b716-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b716-130">RELATED LINKS</span></span>

[<span data-ttu-id="9b716-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="9b716-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="9b716-132">Nowe — AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="9b716-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
