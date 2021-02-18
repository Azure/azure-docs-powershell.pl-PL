---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192875"
---
# <span data-ttu-id="1d427-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="1d427-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="1d427-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d427-102">SYNOPSIS</span></span>
<span data-ttu-id="1d427-103">Tworzy obiekt mapowania dysku dla dysków maszyn wirtualnych vMWare, które mają zostać zreplikowane.</span><span class="sxs-lookup"><span data-stu-id="1d427-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="1d427-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1d427-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d427-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1d427-105">DESCRIPTION</span></span>
<span data-ttu-id="1d427-106">Tworzy obiekt mapowania dysku, który mapuje dysk maszyny wirtualnej vMWare na konto pamięci podręcznej i docelowy zarządzany typ dysku (region odzyskiwania), który ma być używany do replikowania dysku.</span><span class="sxs-lookup"><span data-stu-id="1d427-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="1d427-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1d427-107">EXAMPLES</span></span>

### <span data-ttu-id="1d427-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d427-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="1d427-109">Utwórz obiekt mapowania dysku, aby zreplikować dysk w maszynce wirtualnej vMWare. Używany podczas włączania ochrony dla komputera vMWare.</span><span class="sxs-lookup"><span data-stu-id="1d427-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="1d427-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d427-110">PARAMETERS</span></span>

### <span data-ttu-id="1d427-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d427-111">-DefaultProfile</span></span>
<span data-ttu-id="1d427-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d427-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d427-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="1d427-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="1d427-114">Określa identyfikator zasobu zestawu szyfrowania dysku, który ma być używany do szyfrowania zarządzanych dysków.</span><span class="sxs-lookup"><span data-stu-id="1d427-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="1d427-115">- DiskId</span><span class="sxs-lookup"><span data-stu-id="1d427-115">-DiskId</span></span>
<span data-ttu-id="1d427-116">Określ wartość DiskId dysku, do których odpowiada dane mapowanie.</span><span class="sxs-lookup"><span data-stu-id="1d427-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="1d427-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="1d427-117">-DiskType</span></span>
<span data-ttu-id="1d427-118">Określa typ dysku odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1d427-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="1d427-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1d427-119">-LogStorageAccountId</span></span>
<span data-ttu-id="1d427-120">Określa identyfikator konta magazynu w dzienniku lub pamięci podręcznej, który ma być używany do przechowywania dzienników replikacji.</span><span class="sxs-lookup"><span data-stu-id="1d427-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="1d427-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d427-121">-Confirm</span></span>
<span data-ttu-id="1d427-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1d427-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d427-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d427-123">-WhatIf</span></span>
<span data-ttu-id="1d427-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d427-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d427-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1d427-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d427-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d427-126">CommonParameters</span></span>
<span data-ttu-id="1d427-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d427-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d427-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d427-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d427-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d427-129">INPUTS</span></span>

### <span data-ttu-id="1d427-130">Brak</span><span class="sxs-lookup"><span data-stu-id="1d427-130">None</span></span>

## <span data-ttu-id="1d427-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d427-131">OUTPUTS</span></span>

### <span data-ttu-id="1d427-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2ChatInput</span><span class="sxs-lookup"><span data-stu-id="1d427-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="1d427-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1d427-133">NOTES</span></span>

## <span data-ttu-id="1d427-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d427-134">RELATED LINKS</span></span>
