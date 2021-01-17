---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490022"
---
# <span data-ttu-id="5199a-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="5199a-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="5199a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5199a-102">SYNOPSIS</span></span>
<span data-ttu-id="5199a-103">Pobiera szczegóły kopii zapasowej plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="5199a-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="5199a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5199a-104">SYNTAX</span></span>

### <span data-ttu-id="5199a-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5199a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5199a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5199a-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5199a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5199a-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5199a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5199a-108">DESCRIPTION</span></span>
<span data-ttu-id="5199a-109">Polecenie cmdlet **Get-AzNetAppFilesBackup** pobiera szczegóły ANF kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="5199a-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="5199a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5199a-110">EXAMPLES</span></span>

### <span data-ttu-id="5199a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5199a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="5199a-112">To polecenie pobiera backcup o nazwie "MyAnfAccount" z woluminu o nazwie "Moja głośność".</span><span class="sxs-lookup"><span data-stu-id="5199a-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="5199a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5199a-113">PARAMETERS</span></span>

### <span data-ttu-id="5199a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5199a-114">-AccountName</span></span>
<span data-ttu-id="5199a-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="5199a-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="5199a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5199a-116">-DefaultProfile</span></span>
<span data-ttu-id="5199a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5199a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5199a-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5199a-118">-Name</span></span>
<span data-ttu-id="5199a-119">Nazwa kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="5199a-119">The name of the ANF backup</span></span>

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

### <span data-ttu-id="5199a-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5199a-120">-PoolName</span></span>
<span data-ttu-id="5199a-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="5199a-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="5199a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5199a-122">-ResourceGroupName</span></span>
<span data-ttu-id="5199a-123">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="5199a-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="5199a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5199a-124">-ResourceId</span></span>
<span data-ttu-id="5199a-125">Identyfikator zasobu kopii zapasowej ANF</span><span class="sxs-lookup"><span data-stu-id="5199a-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="5199a-126">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="5199a-126">-VolumeName</span></span>
<span data-ttu-id="5199a-127">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="5199a-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="5199a-128">-Woluminobject</span><span class="sxs-lookup"><span data-stu-id="5199a-128">-VolumeObject</span></span>
<span data-ttu-id="5199a-129">Obiekt woluminu zawierający kopię zapasową do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="5199a-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="5199a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5199a-130">CommonParameters</span></span>
<span data-ttu-id="5199a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5199a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5199a-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5199a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5199a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5199a-133">INPUTS</span></span>

### <span data-ttu-id="5199a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5199a-134">System.String</span></span>

### <span data-ttu-id="5199a-135">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5199a-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="5199a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5199a-136">OUTPUTS</span></span>

### <span data-ttu-id="5199a-137">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="5199a-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="5199a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5199a-138">NOTES</span></span>

## <span data-ttu-id="5199a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5199a-139">RELATED LINKS</span></span>
