---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 30d525ebcb7d80a24e11080ee265eb509f575ff6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372738"
---
# <span data-ttu-id="6b753-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="6b753-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="6b753-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b753-102">SYNOPSIS</span></span>
<span data-ttu-id="6b753-103">Zmień pulę dla woluminu Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="6b753-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="6b753-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b753-104">SYNTAX</span></span>

### <span data-ttu-id="6b753-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6b753-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b753-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b753-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b753-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b753-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b753-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b753-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b753-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6b753-109">DESCRIPTION</span></span>
<span data-ttu-id="6b753-110">Polecenie cmdlet **Set-AzNetAppFilesVolumePool** zmienia pulę woluminu ANF.</span><span class="sxs-lookup"><span data-stu-id="6b753-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="6b753-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b753-111">EXAMPLES</span></span>

### <span data-ttu-id="6b753-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6b753-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="6b753-113">Spowoduje to zmianę puli woluminu na wolumin o identyfikatorze 7d6e4069-6c78-6c61-7bf6-c60968e45fbf.</span><span class="sxs-lookup"><span data-stu-id="6b753-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="6b753-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b753-114">PARAMETERS</span></span>

### <span data-ttu-id="6b753-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6b753-115">-AccountName</span></span>
<span data-ttu-id="6b753-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="6b753-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="6b753-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b753-117">-DefaultProfile</span></span>
<span data-ttu-id="6b753-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b753-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b753-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6b753-119">-InputObject</span></span>
<span data-ttu-id="6b753-120">Obiekt woluminu do przeniesienia</span><span class="sxs-lookup"><span data-stu-id="6b753-120">The volume object to move</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b753-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b753-121">-Name</span></span>
<span data-ttu-id="6b753-122">Nazwa woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="6b753-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b753-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="6b753-123">-NewPoolResourceId</span></span>
<span data-ttu-id="6b753-124">Identyfikator zasobu puli zdoln. do przeniesienia.</span><span class="sxs-lookup"><span data-stu-id="6b753-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="6b753-125">Identyfikator UUID (wersja 4) służący do identyfikowania puli</span><span class="sxs-lookup"><span data-stu-id="6b753-125">UUID v4 used to identify the pool</span></span>

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

### <span data-ttu-id="6b753-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6b753-126">-PoolName</span></span>
<span data-ttu-id="6b753-127">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="6b753-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="6b753-128">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="6b753-128">-PoolObject</span></span>
<span data-ttu-id="6b753-129">Obiekt Pool zawierający wolumin</span><span class="sxs-lookup"><span data-stu-id="6b753-129">The pool object containing the volume</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b753-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b753-130">-ResourceGroupName</span></span>
<span data-ttu-id="6b753-131">Grupa zasobów woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="6b753-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="6b753-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b753-132">-ResourceId</span></span>
<span data-ttu-id="6b753-133">Identyfikator zasobu woluminu ANF</span><span class="sxs-lookup"><span data-stu-id="6b753-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="6b753-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b753-134">-Confirm</span></span>
<span data-ttu-id="6b753-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b753-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b753-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b753-136">-WhatIf</span></span>
<span data-ttu-id="6b753-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b753-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b753-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6b753-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b753-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b753-139">CommonParameters</span></span>
<span data-ttu-id="6b753-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b753-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b753-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b753-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b753-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b753-142">INPUTS</span></span>

### <span data-ttu-id="6b753-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6b753-143">System.String</span></span>

### <span data-ttu-id="6b753-144">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="6b753-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="6b753-145">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6b753-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6b753-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b753-146">OUTPUTS</span></span>

### <span data-ttu-id="6b753-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b753-147">System.Boolean</span></span>

## <span data-ttu-id="6b753-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b753-148">NOTES</span></span>

## <span data-ttu-id="6b753-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b753-149">RELATED LINKS</span></span>
