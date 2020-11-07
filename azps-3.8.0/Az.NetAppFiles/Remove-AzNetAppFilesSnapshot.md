---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 098f38f259db3eeb79b40dc799845877f5cafb60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894189"
---
# <span data-ttu-id="48e2a-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="48e2a-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="48e2a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="48e2a-103">Usuwa migawkę plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="48e2a-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="48e2a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48e2a-104">SYNTAX</span></span>

### <span data-ttu-id="48e2a-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="48e2a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48e2a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48e2a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48e2a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48e2a-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48e2a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48e2a-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48e2a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="48e2a-109">DESCRIPTION</span></span>
<span data-ttu-id="48e2a-110">Polecenie cmdlet **Remove-AzNetAppFilesSnapshot** usuwa migawkę ANF.</span><span class="sxs-lookup"><span data-stu-id="48e2a-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="48e2a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48e2a-111">EXAMPLES</span></span>

### <span data-ttu-id="48e2a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="48e2a-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="48e2a-113">To polecenie usuwa migawkę ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="48e2a-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="48e2a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48e2a-114">PARAMETERS</span></span>

### <span data-ttu-id="48e2a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="48e2a-115">-AccountName</span></span>
<span data-ttu-id="48e2a-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="48e2a-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e2a-117">-DefaultProfile</span></span>
<span data-ttu-id="48e2a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48e2a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="48e2a-119">-InputObject</span></span>
<span data-ttu-id="48e2a-120">Obiekt migawki do usunięcia</span><span class="sxs-lookup"><span data-stu-id="48e2a-120">The snapshot object to remove</span></span>

```yaml
Type: PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48e2a-121">-Name</span></span>
<span data-ttu-id="48e2a-122">Nazwa migawki ANF</span><span class="sxs-lookup"><span data-stu-id="48e2a-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48e2a-123">-PassThru</span></span>
<span data-ttu-id="48e2a-124">Zwracanie, czy określony wolumin został pomyślnie usunięty</span><span class="sxs-lookup"><span data-stu-id="48e2a-124">Return whether the specified volume was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="48e2a-125">-PoolName</span></span>
<span data-ttu-id="48e2a-126">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="48e2a-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e2a-127">-ResourceGroupName</span></span>
<span data-ttu-id="48e2a-128">Grupa zasobów migawki ANF</span><span class="sxs-lookup"><span data-stu-id="48e2a-128">The resource group of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48e2a-129">-ResourceId</span></span>
<span data-ttu-id="48e2a-130">Identyfikator zasobu migawki ANF</span><span class="sxs-lookup"><span data-stu-id="48e2a-130">The resource id of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-131">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="48e2a-131">-VolumeName</span></span>
<span data-ttu-id="48e2a-132">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="48e2a-132">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-133">-Woluminobject</span><span class="sxs-lookup"><span data-stu-id="48e2a-133">-VolumeObject</span></span>
<span data-ttu-id="48e2a-134">Obiekt woluminu zawierający migawkę do usunięcia</span><span class="sxs-lookup"><span data-stu-id="48e2a-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48e2a-135">-Confirm</span></span>
<span data-ttu-id="48e2a-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48e2a-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48e2a-137">-WhatIf</span></span>
<span data-ttu-id="48e2a-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48e2a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48e2a-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="48e2a-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e2a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e2a-140">CommonParameters</span></span>
<span data-ttu-id="48e2a-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48e2a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="48e2a-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48e2a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e2a-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48e2a-143">INPUTS</span></span>

### <span data-ttu-id="48e2a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="48e2a-144">System.String</span></span>

### <span data-ttu-id="48e2a-145">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="48e2a-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="48e2a-146">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="48e2a-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="48e2a-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48e2a-147">OUTPUTS</span></span>

### <span data-ttu-id="48e2a-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48e2a-148">System.Boolean</span></span>

## <span data-ttu-id="48e2a-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48e2a-149">NOTES</span></span>

## <span data-ttu-id="48e2a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48e2a-150">RELATED LINKS</span></span>
