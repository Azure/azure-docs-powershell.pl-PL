---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184850"
---
# <span data-ttu-id="67a6e-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="67a6e-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="67a6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="67a6e-103">Tworzy nową kopię zapasową plików AZURE NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="67a6e-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="67a6e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67a6e-104">SYNTAX</span></span>

### <span data-ttu-id="67a6e-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="67a6e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67a6e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67a6e-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67a6e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="67a6e-107">DESCRIPTION</span></span>
<span data-ttu-id="67a6e-108">Polecenie **cmdlet New-AzNetAppFilesBackup** tworzy kopię zapasową dla woluminu ANF.</span><span class="sxs-lookup"><span data-stu-id="67a6e-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="67a6e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67a6e-109">EXAMPLES</span></span>

### <span data-ttu-id="67a6e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67a6e-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="67a6e-111">To polecenie tworzy nową kopię zapasową ANF dla konta o nazwie "MyVolume".</span><span class="sxs-lookup"><span data-stu-id="67a6e-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="67a6e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67a6e-112">PARAMETERS</span></span>

### <span data-ttu-id="67a6e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="67a6e-113">-AccountName</span></span>
<span data-ttu-id="67a6e-114">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="67a6e-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="67a6e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a6e-115">-DefaultProfile</span></span>
<span data-ttu-id="67a6e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67a6e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67a6e-117">— Label</span><span class="sxs-lookup"><span data-stu-id="67a6e-117">-Label</span></span>
<span data-ttu-id="67a6e-118">Etykieta kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="67a6e-118">Label for backup</span></span>

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

### <span data-ttu-id="67a6e-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="67a6e-119">-Location</span></span>
<span data-ttu-id="67a6e-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="67a6e-120">The location of the resource</span></span>

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

### <span data-ttu-id="67a6e-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="67a6e-121">-Name</span></span>
<span data-ttu-id="67a6e-122">Nazwa kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="67a6e-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a6e-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="67a6e-123">-PoolName</span></span>
<span data-ttu-id="67a6e-124">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="67a6e-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="67a6e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67a6e-125">-ResourceGroupName</span></span>
<span data-ttu-id="67a6e-126">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="67a6e-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="67a6e-127">— VolumeName</span><span class="sxs-lookup"><span data-stu-id="67a6e-127">-VolumeName</span></span>
<span data-ttu-id="67a6e-128">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="67a6e-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="67a6e-129">— VolumeObject</span><span class="sxs-lookup"><span data-stu-id="67a6e-129">-VolumeObject</span></span>
<span data-ttu-id="67a6e-130">Głośność nowego obiektu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="67a6e-130">The volume for the new backup object</span></span>

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

### <span data-ttu-id="67a6e-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67a6e-131">-Confirm</span></span>
<span data-ttu-id="67a6e-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="67a6e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67a6e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a6e-133">-WhatIf</span></span>
<span data-ttu-id="67a6e-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67a6e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67a6e-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="67a6e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67a6e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a6e-136">CommonParameters</span></span>
<span data-ttu-id="67a6e-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a6e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a6e-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67a6e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a6e-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67a6e-139">INPUTS</span></span>

### <span data-ttu-id="67a6e-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="67a6e-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="67a6e-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67a6e-141">OUTPUTS</span></span>

### <span data-ttu-id="67a6e-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="67a6e-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="67a6e-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67a6e-143">NOTES</span></span>

## <span data-ttu-id="67a6e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67a6e-144">RELATED LINKS</span></span>
