---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187290"
---
# <span data-ttu-id="efac1-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="efac1-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="efac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efac1-102">SYNOPSIS</span></span>
<span data-ttu-id="efac1-103">Pobiera szczegółowe informacje o kopii zapasowej plików ANF (Azure NetApp Files).</span><span class="sxs-lookup"><span data-stu-id="efac1-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="efac1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="efac1-104">SYNTAX</span></span>

### <span data-ttu-id="efac1-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="efac1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efac1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efac1-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="efac1-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efac1-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efac1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="efac1-108">DESCRIPTION</span></span>
<span data-ttu-id="efac1-109">Polecenie **cmdlet Get-AzNetAppFilesBackup** pobiera szczegóły dotyczące kopii zapasowej ANF.</span><span class="sxs-lookup"><span data-stu-id="efac1-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="efac1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="efac1-110">EXAMPLES</span></span>

### <span data-ttu-id="efac1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="efac1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="efac1-112">To polecenie pobiera nazwę backcup o nazwie "MyAnfAccount" z poziomu woluminu o nazwie "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="efac1-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="efac1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efac1-113">PARAMETERS</span></span>

### <span data-ttu-id="efac1-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="efac1-114">-AccountName</span></span>
<span data-ttu-id="efac1-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="efac1-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efac1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efac1-116">-DefaultProfile</span></span>
<span data-ttu-id="efac1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="efac1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efac1-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="efac1-118">-Name</span></span>
<span data-ttu-id="efac1-119">Nazwa kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="efac1-119">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efac1-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="efac1-120">-PoolName</span></span>
<span data-ttu-id="efac1-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="efac1-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efac1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efac1-122">-ResourceGroupName</span></span>
<span data-ttu-id="efac1-123">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="efac1-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efac1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efac1-124">-ResourceId</span></span>
<span data-ttu-id="efac1-125">Identyfikator zasobu kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="efac1-125">The resource id of the ANF Backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efac1-126">— VolumeName</span><span class="sxs-lookup"><span data-stu-id="efac1-126">-VolumeName</span></span>
<span data-ttu-id="efac1-127">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="efac1-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efac1-128">— VolumeObject</span><span class="sxs-lookup"><span data-stu-id="efac1-128">-VolumeObject</span></span>
<span data-ttu-id="efac1-129">Obiekt głośności zawierający kopię zapasową do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="efac1-129">The volume object containing the backup to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efac1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efac1-130">CommonParameters</span></span>
<span data-ttu-id="efac1-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efac1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efac1-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efac1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efac1-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efac1-133">INPUTS</span></span>

### <span data-ttu-id="efac1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="efac1-134">System.String</span></span>

### <span data-ttu-id="efac1-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="efac1-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="efac1-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="efac1-136">OUTPUTS</span></span>

### <span data-ttu-id="efac1-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="efac1-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="efac1-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="efac1-138">NOTES</span></span>

## <span data-ttu-id="efac1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efac1-139">RELATED LINKS</span></span>
