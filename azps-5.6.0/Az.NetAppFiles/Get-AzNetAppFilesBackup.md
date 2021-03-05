---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 8a4183c148eda0f5f560d24c2b5874ff5577e85e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968634"
---
# <span data-ttu-id="8fb3d-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="8fb3d-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="8fb3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fb3d-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb3d-103">Pobiera szczegółowe informacje o kopii zapasowej plików ANF (Azure NetApp Files).</span><span class="sxs-lookup"><span data-stu-id="8fb3d-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="8fb3d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8fb3d-104">SYNTAX</span></span>

### <span data-ttu-id="8fb3d-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8fb3d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fb3d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fb3d-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fb3d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fb3d-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fb3d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8fb3d-108">DESCRIPTION</span></span>
<span data-ttu-id="8fb3d-109">Polecenie **cmdlet Get-AzNetAppFilesBackup** pobiera szczegóły dotyczące kopii zapasowej ANF.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="8fb3d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8fb3d-110">EXAMPLES</span></span>

### <span data-ttu-id="8fb3d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8fb3d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="8fb3d-112">To polecenie pobiera nazwę backcup o nazwie "MyAnfAccount" z poziomu woluminu o nazwie "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="8fb3d-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="8fb3d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fb3d-113">PARAMETERS</span></span>

### <span data-ttu-id="8fb3d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8fb3d-114">-AccountName</span></span>
<span data-ttu-id="8fb3d-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="8fb3d-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="8fb3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb3d-116">-DefaultProfile</span></span>
<span data-ttu-id="8fb3d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fb3d-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8fb3d-118">-Name</span></span>
<span data-ttu-id="8fb3d-119">Nazwa kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="8fb3d-119">The name of the ANF backup</span></span>

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

### <span data-ttu-id="8fb3d-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8fb3d-120">-PoolName</span></span>
<span data-ttu-id="8fb3d-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="8fb3d-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8fb3d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fb3d-122">-ResourceGroupName</span></span>
<span data-ttu-id="8fb3d-123">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="8fb3d-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8fb3d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fb3d-124">-ResourceId</span></span>
<span data-ttu-id="8fb3d-125">Identyfikator zasobu kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="8fb3d-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="8fb3d-126">— VolumeName</span><span class="sxs-lookup"><span data-stu-id="8fb3d-126">-VolumeName</span></span>
<span data-ttu-id="8fb3d-127">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="8fb3d-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="8fb3d-128">— VolumeObject</span><span class="sxs-lookup"><span data-stu-id="8fb3d-128">-VolumeObject</span></span>
<span data-ttu-id="8fb3d-129">Obiekt woluminu zawierający kopię zapasową do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="8fb3d-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="8fb3d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb3d-130">CommonParameters</span></span>
<span data-ttu-id="8fb3d-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fb3d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb3d-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fb3d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb3d-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fb3d-133">INPUTS</span></span>

### <span data-ttu-id="8fb3d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8fb3d-134">System.String</span></span>

### <span data-ttu-id="8fb3d-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8fb3d-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8fb3d-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fb3d-136">OUTPUTS</span></span>

### <span data-ttu-id="8fb3d-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="8fb3d-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="8fb3d-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8fb3d-138">NOTES</span></span>

## <span data-ttu-id="8fb3d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fb3d-139">RELATED LINKS</span></span>
