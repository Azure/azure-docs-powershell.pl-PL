---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 095759ca2753cac4f7155430a241e0554e910fd6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500017"
---
# <span data-ttu-id="3f5e7-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3f5e7-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="3f5e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5e7-103">Usuwa określoną sieć szkieletową odzyskiwania witryny platformy Azure z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="3f5e7-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="3f5e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f5e7-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f5e7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f5e7-105">DESCRIPTION</span></span>
<span data-ttu-id="3f5e7-106">Polecenie cmdlet **Remove-AzRecoveryServicesAsrFabric** usuwa określoną sieć szkieletową odzyskiwania witryny platformy Azure z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="3f5e7-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="3f5e7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f5e7-107">EXAMPLES</span></span>

### <span data-ttu-id="3f5e7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3f5e7-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="3f5e7-109">Rozpoczyna usuwanie określonej sieci szkieletowej i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="3f5e7-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3f5e7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f5e7-110">PARAMETERS</span></span>

### <span data-ttu-id="3f5e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5e7-111">-DefaultProfile</span></span>
<span data-ttu-id="3f5e7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f5e7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3f5e7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3f5e7-113">-Force</span></span>
<span data-ttu-id="3f5e7-114">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="3f5e7-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="3f5e7-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3f5e7-115">-InputObject</span></span>
<span data-ttu-id="3f5e7-116">Obiekt wejściowy do polecenia cmdlet: obiekt sieci szkieletowej ASR odpowiadający sieci szkieletowej, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="3f5e7-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="3f5e7-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3f5e7-117">-Confirm</span></span>
<span data-ttu-id="3f5e7-118">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="3f5e7-118">Specify if confirmation is required.</span></span> <span data-ttu-id="3f5e7-119">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3f5e7-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="3f5e7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f5e7-120">-WhatIf</span></span>
<span data-ttu-id="3f5e7-121">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f5e7-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="3f5e7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5e7-122">CommonParameters</span></span>
<span data-ttu-id="3f5e7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f5e7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5e7-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f5e7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5e7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f5e7-125">INPUTS</span></span>

### <span data-ttu-id="3f5e7-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="3f5e7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="3f5e7-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f5e7-127">OUTPUTS</span></span>

### <span data-ttu-id="3f5e7-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3f5e7-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3f5e7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f5e7-129">NOTES</span></span>

## <span data-ttu-id="3f5e7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f5e7-130">RELATED LINKS</span></span>

[<span data-ttu-id="3f5e7-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3f5e7-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="3f5e7-132">Nowe — AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="3f5e7-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
