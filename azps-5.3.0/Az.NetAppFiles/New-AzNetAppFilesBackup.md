---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489986"
---
# <span data-ttu-id="d6efb-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="d6efb-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="d6efb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6efb-102">SYNOPSIS</span></span>
<span data-ttu-id="d6efb-103">Tworzy nową kopię zapasową plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="d6efb-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="d6efb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6efb-104">SYNTAX</span></span>

### <span data-ttu-id="d6efb-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d6efb-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6efb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6efb-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6efb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d6efb-107">DESCRIPTION</span></span>
<span data-ttu-id="d6efb-108">Polecenie cmdlet **New-AzNetAppFilesBackup** tworzy kopię zapasową dla woluminu ANF.</span><span class="sxs-lookup"><span data-stu-id="d6efb-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="d6efb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6efb-109">EXAMPLES</span></span>

### <span data-ttu-id="d6efb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6efb-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="d6efb-111">To polecenie tworzy nową ANF kopię zapasową dla woluminu o nazwie "Moja głośność".</span><span class="sxs-lookup"><span data-stu-id="d6efb-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="d6efb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6efb-112">PARAMETERS</span></span>

### <span data-ttu-id="d6efb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d6efb-113">-AccountName</span></span>
<span data-ttu-id="d6efb-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="d6efb-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="d6efb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6efb-115">-DefaultProfile</span></span>
<span data-ttu-id="d6efb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6efb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6efb-117">-Label</span><span class="sxs-lookup"><span data-stu-id="d6efb-117">-Label</span></span>
<span data-ttu-id="d6efb-118">Etykieta kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="d6efb-118">Label for backup</span></span>

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

### <span data-ttu-id="d6efb-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d6efb-119">-Location</span></span>
<span data-ttu-id="d6efb-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="d6efb-120">The location of the resource</span></span>

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

### <span data-ttu-id="d6efb-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6efb-121">-Name</span></span>
<span data-ttu-id="d6efb-122">Nazwa kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="d6efb-122">The name of the ANF backup</span></span>

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

### <span data-ttu-id="d6efb-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d6efb-123">-PoolName</span></span>
<span data-ttu-id="d6efb-124">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="d6efb-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d6efb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6efb-125">-ResourceGroupName</span></span>
<span data-ttu-id="d6efb-126">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="d6efb-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d6efb-127">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="d6efb-127">-VolumeName</span></span>
<span data-ttu-id="d6efb-128">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="d6efb-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="d6efb-129">-Woluminobject</span><span class="sxs-lookup"><span data-stu-id="d6efb-129">-VolumeObject</span></span>
<span data-ttu-id="d6efb-130">Wolumin nowego obiektu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="d6efb-130">The volume for the new backup object</span></span>

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

### <span data-ttu-id="d6efb-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6efb-131">-Confirm</span></span>
<span data-ttu-id="d6efb-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6efb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6efb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6efb-133">-WhatIf</span></span>
<span data-ttu-id="d6efb-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6efb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6efb-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d6efb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6efb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6efb-136">CommonParameters</span></span>
<span data-ttu-id="d6efb-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6efb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6efb-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6efb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6efb-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6efb-139">INPUTS</span></span>

### <span data-ttu-id="d6efb-140">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d6efb-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d6efb-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6efb-141">OUTPUTS</span></span>

### <span data-ttu-id="d6efb-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="d6efb-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="d6efb-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6efb-143">NOTES</span></span>

## <span data-ttu-id="d6efb-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6efb-144">RELATED LINKS</span></span>
