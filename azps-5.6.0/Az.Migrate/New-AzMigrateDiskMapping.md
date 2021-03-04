---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 1fc58ff016c41e693c059ce792a8dc8aa06e0d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982778"
---
# <span data-ttu-id="75521-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="75521-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="75521-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75521-102">SYNOPSIS</span></span>
<span data-ttu-id="75521-103">Tworzy nowe mapowanie dysku</span><span class="sxs-lookup"><span data-stu-id="75521-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="75521-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="75521-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <String> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="75521-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="75521-105">DESCRIPTION</span></span>
<span data-ttu-id="75521-106">Polecenie New-AzMigrateDiskMapping cmdlet tworzy mapowanie dysku źródłowego dołączonego do serwera do migrowania</span><span class="sxs-lookup"><span data-stu-id="75521-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="75521-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="75521-107">EXAMPLES</span></span>

### <span data-ttu-id="75521-108">Przykład 1. Na dyskach</span><span class="sxs-lookup"><span data-stu-id="75521-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="75521-109">Uzyskaj obiekt dyskietki, aby wprowadzić dane New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="75521-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="75521-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75521-110">PARAMETERS</span></span>

### <span data-ttu-id="75521-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="75521-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="75521-112">Określa zestaw encypcji dysku, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="75521-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="75521-113">— DiskID</span><span class="sxs-lookup"><span data-stu-id="75521-113">-DiskID</span></span>
<span data-ttu-id="75521-114">Określa identyfikator dysku dołączonego do serwera, który ma zostać podmigrowany.</span><span class="sxs-lookup"><span data-stu-id="75521-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="75521-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="75521-115">-DiskType</span></span>
<span data-ttu-id="75521-116">Określa typ dysków, które mają być używane dla maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="75521-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="75521-117">-IsOS Jednakowy</span><span class="sxs-lookup"><span data-stu-id="75521-117">-IsOSDisk</span></span>
<span data-ttu-id="75521-118">Określa, czy dysk zawiera system operacyjny dla serwera źródłowego, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="75521-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="75521-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75521-119">CommonParameters</span></span>
<span data-ttu-id="75521-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75521-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75521-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75521-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75521-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75521-122">INPUTS</span></span>

## <span data-ttu-id="75521-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75521-123">OUTPUTS</span></span>

### <span data-ttu-id="75521-124">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.IV JakAsłoŃCbt Jednakowe</span><span class="sxs-lookup"><span data-stu-id="75521-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="75521-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="75521-125">NOTES</span></span>

<span data-ttu-id="75521-126">ALIASY</span><span class="sxs-lookup"><span data-stu-id="75521-126">ALIASES</span></span>

## <span data-ttu-id="75521-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75521-127">RELATED LINKS</span></span>

