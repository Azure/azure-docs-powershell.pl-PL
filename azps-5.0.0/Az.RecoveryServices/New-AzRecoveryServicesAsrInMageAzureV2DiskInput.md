---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232949"
---
# <span data-ttu-id="58a99-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="58a99-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="58a99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58a99-102">SYNOPSIS</span></span>
<span data-ttu-id="58a99-103">Tworzy obiekt mapowania dysku na potrzeby replikowania dysków maszyny wirtualnej vMWare.</span><span class="sxs-lookup"><span data-stu-id="58a99-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="58a99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58a99-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58a99-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58a99-105">DESCRIPTION</span></span>
<span data-ttu-id="58a99-106">Tworzy obiekt mapowania dysku, który mapuje dysk maszyny wirtualnej vMWare na konto magazynu pamięci podręcznej oraz docelowy typ dysku zarządzanego (region odzyskiwania), który ma być wykorzystywany do replikowania dysku.</span><span class="sxs-lookup"><span data-stu-id="58a99-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="58a99-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58a99-107">EXAMPLES</span></span>

### <span data-ttu-id="58a99-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58a99-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="58a99-109">Utwórz obiekt mapowania dysku na potrzeby replikowania dysków maszyny wirtualnej vMWare. Używane podczas włączania ochrony dla programu vMWare Machine.</span><span class="sxs-lookup"><span data-stu-id="58a99-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="58a99-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58a99-110">PARAMETERS</span></span>

### <span data-ttu-id="58a99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a99-111">-DefaultProfile</span></span>
<span data-ttu-id="58a99-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58a99-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58a99-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="58a99-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="58a99-114">Określa identyfikator zasobu zestawu szyfrowanie dysków, który ma być wykorzystywany do szyfrowania zarządzanych dysków.</span><span class="sxs-lookup"><span data-stu-id="58a99-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="58a99-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="58a99-115">-DiskId</span></span>
<span data-ttu-id="58a99-116">Określ DiskId dysku, do którego odnosi się to mapowanie.</span><span class="sxs-lookup"><span data-stu-id="58a99-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="58a99-117">-Disktype</span><span class="sxs-lookup"><span data-stu-id="58a99-117">-DiskType</span></span>
<span data-ttu-id="58a99-118">Określa typ dysku odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="58a99-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="58a99-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="58a99-119">-LogStorageAccountId</span></span>
<span data-ttu-id="58a99-120">Określa identyfikator konta dziennika lub pamięci podręcznej, który ma być wykorzystywany do przechowywania dzienników replikacji.</span><span class="sxs-lookup"><span data-stu-id="58a99-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="58a99-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58a99-121">-Confirm</span></span>
<span data-ttu-id="58a99-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58a99-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a99-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58a99-123">-WhatIf</span></span>
<span data-ttu-id="58a99-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58a99-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58a99-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58a99-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58a99-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a99-126">CommonParameters</span></span>
<span data-ttu-id="58a99-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a99-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a99-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58a99-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a99-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58a99-129">INPUTS</span></span>

### <span data-ttu-id="58a99-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="58a99-130">None</span></span>

## <span data-ttu-id="58a99-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58a99-131">OUTPUTS</span></span>

### <span data-ttu-id="58a99-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="58a99-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="58a99-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58a99-133">NOTES</span></span>

## <span data-ttu-id="58a99-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58a99-134">RELATED LINKS</span></span>
