---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8dcab2bcaeafbc5304de72b8bcf539a6f4a53934
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240251"
---
# <span data-ttu-id="5abeb-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5abeb-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="5abeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5abeb-102">SYNOPSIS</span></span>
<span data-ttu-id="5abeb-103">Usuwa wskazane mapowanie klasyfikacji magazynu asr.</span><span class="sxs-lookup"><span data-stu-id="5abeb-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="5abeb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5abeb-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5abeb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5abeb-105">DESCRIPTION</span></span>
<span data-ttu-id="5abeb-106">Polecenie **cmdlet Remove-AzRecoveryServicesAsrStorageClassificationMapping** usuwa wskazane mapowanie klasyfikacji magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5abeb-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="5abeb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5abeb-107">EXAMPLES</span></span>

### <span data-ttu-id="5abeb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5abeb-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="5abeb-109">Rozpoczyna usuwanie mapowania określonej klasyfikacji magazynu i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="5abeb-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5abeb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5abeb-110">PARAMETERS</span></span>

### <span data-ttu-id="5abeb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5abeb-111">-DefaultProfile</span></span>
<span data-ttu-id="5abeb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5abeb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5abeb-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5abeb-113">-InputObject</span></span>
<span data-ttu-id="5abeb-114">Obiekt wejściowy do polecenia cmdlet: Obiekt mapowania klasyfikacji magazynu asr odpowiadający mapowaniu klasyfikacji magazynu asr do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5abeb-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5abeb-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5abeb-115">-Confirm</span></span>
<span data-ttu-id="5abeb-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5abeb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5abeb-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5abeb-117">-WhatIf</span></span>
<span data-ttu-id="5abeb-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5abeb-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5abeb-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5abeb-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5abeb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5abeb-120">CommonParameters</span></span>
<span data-ttu-id="5abeb-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5abeb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5abeb-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5abeb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5abeb-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5abeb-123">INPUTS</span></span>

### <span data-ttu-id="5abeb-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5abeb-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="5abeb-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5abeb-125">OUTPUTS</span></span>

### <span data-ttu-id="5abeb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="5abeb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5abeb-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5abeb-127">NOTES</span></span>

## <span data-ttu-id="5abeb-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5abeb-128">RELATED LINKS</span></span>

[<span data-ttu-id="5abeb-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5abeb-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="5abeb-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="5abeb-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
