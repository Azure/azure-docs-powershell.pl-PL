---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385763"
---
# <span data-ttu-id="63f5f-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="63f5f-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="63f5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="63f5f-103">Tworzy nowe mapowanie dysku</span><span class="sxs-lookup"><span data-stu-id="63f5f-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="63f5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63f5f-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="63f5f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="63f5f-105">DESCRIPTION</span></span>
<span data-ttu-id="63f5f-106">Polecenie cmdlet New-AzMigrateDiskMapping tworzy mapowanie dysku źródłowego podłączonego do serwera, który ma zostać zmigrowany</span><span class="sxs-lookup"><span data-stu-id="63f5f-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="63f5f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63f5f-107">EXAMPLES</span></span>

### <span data-ttu-id="63f5f-108">Przykład 1. Tworzenie dysków</span><span class="sxs-lookup"><span data-stu-id="63f5f-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="63f5f-109">Obiekt Pobierz dyski, aby wprowadzić dane wejściowe dla New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="63f5f-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="63f5f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63f5f-110">PARAMETERS</span></span>

### <span data-ttu-id="63f5f-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="63f5f-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="63f5f-112">Określa zestaw encyption dysków, który ma być wykorzystywany.</span><span class="sxs-lookup"><span data-stu-id="63f5f-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="63f5f-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="63f5f-113">-DiskID</span></span>
<span data-ttu-id="63f5f-114">Określa identyfikator dysku dołączonego do odnalezionego serwera, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="63f5f-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="63f5f-115">-Disktype</span><span class="sxs-lookup"><span data-stu-id="63f5f-115">-DiskType</span></span>
<span data-ttu-id="63f5f-116">Określa typ dysków, które mają być używane na potrzeby maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="63f5f-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f5f-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="63f5f-117">-IsOSDisk</span></span>
<span data-ttu-id="63f5f-118">Określa, czy dysk zawiera system operacyjny dla serwera źródłowego, który ma zostać zmigrowany.</span><span class="sxs-lookup"><span data-stu-id="63f5f-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="63f5f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f5f-119">CommonParameters</span></span>
<span data-ttu-id="63f5f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f5f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f5f-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63f5f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f5f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63f5f-122">INPUTS</span></span>

## <span data-ttu-id="63f5f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63f5f-123">OUTPUTS</span></span>

### <span data-ttu-id="63f5f-124">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="63f5f-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="63f5f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63f5f-125">NOTES</span></span>

<span data-ttu-id="63f5f-126">PISUJE</span><span class="sxs-lookup"><span data-stu-id="63f5f-126">ALIASES</span></span>

## <span data-ttu-id="63f5f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63f5f-127">RELATED LINKS</span></span>

