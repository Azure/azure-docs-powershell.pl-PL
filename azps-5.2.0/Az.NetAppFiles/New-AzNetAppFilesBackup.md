---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359961"
---
# <span data-ttu-id="86679-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="86679-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="86679-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86679-102">SYNOPSIS</span></span>
<span data-ttu-id="86679-103">Tworzy nową kopię zapasową plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="86679-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="86679-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86679-104">SYNTAX</span></span>

### <span data-ttu-id="86679-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="86679-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86679-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86679-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86679-107">Opis</span><span class="sxs-lookup"><span data-stu-id="86679-107">DESCRIPTION</span></span>
<span data-ttu-id="86679-108">Polecenie cmdlet **New-AzNetAppFilesBackup** tworzy kopię zapasową dla woluminu ANF.</span><span class="sxs-lookup"><span data-stu-id="86679-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="86679-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86679-109">EXAMPLES</span></span>

### <span data-ttu-id="86679-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86679-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="86679-111">To polecenie tworzy nową ANF kopię zapasową dla woluminu o nazwie "Moja głośność".</span><span class="sxs-lookup"><span data-stu-id="86679-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="86679-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86679-112">PARAMETERS</span></span>

### <span data-ttu-id="86679-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="86679-113">-AccountName</span></span>
<span data-ttu-id="86679-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="86679-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="86679-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86679-115">-DefaultProfile</span></span>
<span data-ttu-id="86679-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86679-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86679-117">-Label</span><span class="sxs-lookup"><span data-stu-id="86679-117">-Label</span></span>
<span data-ttu-id="86679-118">Etykieta kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="86679-118">Label for backup</span></span>

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

### <span data-ttu-id="86679-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="86679-119">-Location</span></span>
<span data-ttu-id="86679-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="86679-120">The location of the resource</span></span>

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

### <span data-ttu-id="86679-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86679-121">-Name</span></span>
<span data-ttu-id="86679-122">Nazwa kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="86679-122">The name of the ANF backup</span></span>

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

### <span data-ttu-id="86679-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="86679-123">-PoolName</span></span>
<span data-ttu-id="86679-124">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="86679-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="86679-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86679-125">-ResourceGroupName</span></span>
<span data-ttu-id="86679-126">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="86679-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="86679-127">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="86679-127">-VolumeName</span></span>
<span data-ttu-id="86679-128">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="86679-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="86679-129">-Woluminobject</span><span class="sxs-lookup"><span data-stu-id="86679-129">-VolumeObject</span></span>
<span data-ttu-id="86679-130">Wolumin nowego obiektu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="86679-130">The volume for the new backup object</span></span>

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

### <span data-ttu-id="86679-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86679-131">-Confirm</span></span>
<span data-ttu-id="86679-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86679-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86679-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86679-133">-WhatIf</span></span>
<span data-ttu-id="86679-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86679-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86679-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="86679-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86679-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86679-136">CommonParameters</span></span>
<span data-ttu-id="86679-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86679-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86679-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86679-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86679-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86679-139">INPUTS</span></span>

### <span data-ttu-id="86679-140">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="86679-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="86679-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86679-141">OUTPUTS</span></span>

### <span data-ttu-id="86679-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="86679-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="86679-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86679-143">NOTES</span></span>

## <span data-ttu-id="86679-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86679-144">RELATED LINKS</span></span>
