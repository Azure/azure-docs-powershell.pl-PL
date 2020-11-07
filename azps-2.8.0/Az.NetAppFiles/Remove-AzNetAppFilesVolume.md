---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: f6b21f3496f8ac05147db24de1df2ee03693fb7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870376"
---
# <span data-ttu-id="8e578-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8e578-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="8e578-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e578-102">SYNOPSIS</span></span>
<span data-ttu-id="8e578-103">Usuwa wolumin usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="8e578-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="8e578-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e578-104">SYNTAX</span></span>

### <span data-ttu-id="8e578-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8e578-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e578-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e578-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e578-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e578-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e578-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e578-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e578-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8e578-109">DESCRIPTION</span></span>
<span data-ttu-id="8e578-110">Polecenie cmdlet **Remove-AzNetAppFilesVolume** usuwa wolumin ANF.</span><span class="sxs-lookup"><span data-stu-id="8e578-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="8e578-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e578-111">EXAMPLES</span></span>

### <span data-ttu-id="8e578-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e578-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="8e578-113">To polecenie usuwa wolumin ANF "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="8e578-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="8e578-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e578-114">PARAMETERS</span></span>

### <span data-ttu-id="8e578-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e578-115">-AccountName</span></span>
<span data-ttu-id="8e578-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="8e578-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8e578-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e578-117">-DefaultProfile</span></span>
<span data-ttu-id="8e578-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e578-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e578-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e578-119">-InputObject</span></span>
<span data-ttu-id="8e578-120">Obiekt woluminu do usunięcia</span><span class="sxs-lookup"><span data-stu-id="8e578-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e578-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e578-121">-Name</span></span>
<span data-ttu-id="8e578-122">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="8e578-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e578-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e578-123">-PassThru</span></span>
<span data-ttu-id="8e578-124">Zwracanie, czy określony wolumin został pomyślnie usunięty</span><span class="sxs-lookup"><span data-stu-id="8e578-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="8e578-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8e578-125">-PoolName</span></span>
<span data-ttu-id="8e578-126">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="8e578-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8e578-127">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="8e578-127">-PoolObject</span></span>
<span data-ttu-id="8e578-128">Obiekt Pool zawierający wolumin do usunięcia</span><span class="sxs-lookup"><span data-stu-id="8e578-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e578-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e578-129">-ResourceGroupName</span></span>
<span data-ttu-id="8e578-130">Grupa zasobów woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="8e578-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="8e578-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e578-131">-ResourceId</span></span>
<span data-ttu-id="8e578-132">Identyfikator zasobu woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="8e578-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="8e578-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e578-133">-Confirm</span></span>
<span data-ttu-id="8e578-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e578-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e578-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e578-135">-WhatIf</span></span>
<span data-ttu-id="8e578-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e578-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e578-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e578-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e578-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e578-138">CommonParameters</span></span>
<span data-ttu-id="8e578-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e578-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8e578-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e578-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e578-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e578-141">INPUTS</span></span>

### <span data-ttu-id="8e578-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8e578-142">System.String</span></span>

### <span data-ttu-id="8e578-143">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8e578-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="8e578-144">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8e578-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8e578-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e578-145">OUTPUTS</span></span>

### <span data-ttu-id="8e578-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e578-146">System.Boolean</span></span>

## <span data-ttu-id="8e578-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e578-147">NOTES</span></span>

## <span data-ttu-id="8e578-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e578-148">RELATED LINKS</span></span>
