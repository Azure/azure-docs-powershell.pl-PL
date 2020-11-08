---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1d28420e9457826f7c851eb0d3013f36de9edbc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062637"
---
# <span data-ttu-id="8bdfa-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="8bdfa-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="8bdfa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8bdfa-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdfa-103">Usuwa migawkę plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="8bdfa-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="8bdfa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8bdfa-104">SYNTAX</span></span>

### <span data-ttu-id="8bdfa-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8bdfa-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bdfa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bdfa-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bdfa-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bdfa-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bdfa-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bdfa-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bdfa-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8bdfa-109">DESCRIPTION</span></span>
<span data-ttu-id="8bdfa-110">Polecenie cmdlet **Remove-AzNetAppFilesSnapshot** usuwa migawkę ANF.</span><span class="sxs-lookup"><span data-stu-id="8bdfa-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="8bdfa-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8bdfa-111">EXAMPLES</span></span>

### <span data-ttu-id="8bdfa-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8bdfa-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="8bdfa-113">To polecenie usuwa migawkę ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="8bdfa-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="8bdfa-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8bdfa-114">PARAMETERS</span></span>

### <span data-ttu-id="8bdfa-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8bdfa-115">-AccountName</span></span>
<span data-ttu-id="8bdfa-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="8bdfa-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8bdfa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bdfa-117">-DefaultProfile</span></span>
<span data-ttu-id="8bdfa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bdfa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bdfa-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8bdfa-119">-InputObject</span></span>
<span data-ttu-id="8bdfa-120">Obiekt migawki do usunięcia</span><span class="sxs-lookup"><span data-stu-id="8bdfa-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdfa-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8bdfa-121">-Name</span></span>
<span data-ttu-id="8bdfa-122">Nazwa migawki ANF</span><span class="sxs-lookup"><span data-stu-id="8bdfa-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdfa-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bdfa-123">-PassThru</span></span>
<span data-ttu-id="8bdfa-124">Zwracanie, czy określony wolumin został pomyślnie usunięty</span><span class="sxs-lookup"><span data-stu-id="8bdfa-124">Return whether the specified volume was successfully removed</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdfa-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8bdfa-125">-PoolName</span></span>
<span data-ttu-id="8bdfa-126">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="8bdfa-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8bdfa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bdfa-127">-ResourceGroupName</span></span>
<span data-ttu-id="8bdfa-128">Grupa zasobów migawki ANF</span><span class="sxs-lookup"><span data-stu-id="8bdfa-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="8bdfa-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bdfa-129">-ResourceId</span></span>
<span data-ttu-id="8bdfa-130">Identyfikator zasobu migawki ANF</span><span class="sxs-lookup"><span data-stu-id="8bdfa-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="8bdfa-131">-Nazwa_woluminu</span><span class="sxs-lookup"><span data-stu-id="8bdfa-131">-VolumeName</span></span>
<span data-ttu-id="8bdfa-132">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="8bdfa-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="8bdfa-133">-Woluminobject</span><span class="sxs-lookup"><span data-stu-id="8bdfa-133">-VolumeObject</span></span>
<span data-ttu-id="8bdfa-134">Obiekt woluminu zawierający migawkę do usunięcia</span><span class="sxs-lookup"><span data-stu-id="8bdfa-134">The volume object containing the snapshot to remove</span></span>

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

### <span data-ttu-id="8bdfa-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bdfa-135">-Confirm</span></span>
<span data-ttu-id="8bdfa-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bdfa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bdfa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bdfa-137">-WhatIf</span></span>
<span data-ttu-id="8bdfa-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bdfa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bdfa-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8bdfa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bdfa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdfa-140">CommonParameters</span></span>
<span data-ttu-id="8bdfa-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bdfa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdfa-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bdfa-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdfa-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bdfa-143">INPUTS</span></span>

### <span data-ttu-id="8bdfa-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8bdfa-144">System.String</span></span>

### <span data-ttu-id="8bdfa-145">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8bdfa-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="8bdfa-146">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="8bdfa-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="8bdfa-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8bdfa-147">OUTPUTS</span></span>

### <span data-ttu-id="8bdfa-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8bdfa-148">System.Boolean</span></span>

## <span data-ttu-id="8bdfa-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8bdfa-149">NOTES</span></span>

## <span data-ttu-id="8bdfa-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bdfa-150">RELATED LINKS</span></span>
