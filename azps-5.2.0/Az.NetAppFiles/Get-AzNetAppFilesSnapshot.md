---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 0f1b6806565a21b106816019c08641e269c4d5a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360045"
---
# <span data-ttu-id="ed003-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="ed003-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="ed003-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed003-102">SYNOPSIS</span></span>
<span data-ttu-id="ed003-103">Pobiera szczegóły migawki usługi Azure NetApp plików (ANF).</span><span class="sxs-lookup"><span data-stu-id="ed003-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="ed003-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed003-104">SYNTAX</span></span>

### <span data-ttu-id="ed003-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed003-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed003-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed003-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed003-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed003-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed003-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ed003-108">DESCRIPTION</span></span>
<span data-ttu-id="ed003-109">Polecenie cmdlet **Get-AzNetAppFilesSnapshot** pobiera szczegóły migawki ANF.</span><span class="sxs-lookup"><span data-stu-id="ed003-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="ed003-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed003-110">EXAMPLES</span></span>

### <span data-ttu-id="ed003-111">Przykład 1: uzyskiwanie migawki ANF</span><span class="sxs-lookup"><span data-stu-id="ed003-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="ed003-112">To polecenie uzyskuje migawkę o nazwie MyAnfSnapshot z woluminu "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="ed003-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="ed003-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed003-113">PARAMETERS</span></span>

### <span data-ttu-id="ed003-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed003-114">-AccountName</span></span>
<span data-ttu-id="ed003-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="ed003-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="ed003-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed003-116">-DefaultProfile</span></span>
<span data-ttu-id="ed003-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed003-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed003-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed003-118">-Name</span></span>
<span data-ttu-id="ed003-119">Nazwa migawki ANF</span><span class="sxs-lookup"><span data-stu-id="ed003-119">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed003-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ed003-120">-PoolName</span></span>
<span data-ttu-id="ed003-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="ed003-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="ed003-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed003-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed003-123">Grupa zasobów woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="ed003-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="ed003-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed003-124">-ResourceId</span></span>
<span data-ttu-id="ed003-125">Identyfikator zasobu migawki ANF</span><span class="sxs-lookup"><span data-stu-id="ed003-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="ed003-126">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="ed003-126">-VolumeName</span></span>
<span data-ttu-id="ed003-127">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="ed003-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="ed003-128">-Woluminobject</span><span class="sxs-lookup"><span data-stu-id="ed003-128">-VolumeObject</span></span>
<span data-ttu-id="ed003-129">Obiekt woluminu zawierający migawkę do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="ed003-129">The volume object containing the snapshot to return</span></span>

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

### <span data-ttu-id="ed003-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed003-130">CommonParameters</span></span>
<span data-ttu-id="ed003-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed003-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed003-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed003-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed003-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed003-133">INPUTS</span></span>

### <span data-ttu-id="ed003-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ed003-134">System.String</span></span>

### <span data-ttu-id="ed003-135">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ed003-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ed003-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed003-136">OUTPUTS</span></span>

### <span data-ttu-id="ed003-137">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="ed003-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="ed003-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed003-138">NOTES</span></span>

## <span data-ttu-id="ed003-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed003-139">RELATED LINKS</span></span>
