---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: ef896185b606e107bb62208255a255655814fcbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870380"
---
# <span data-ttu-id="f2fe5-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f2fe5-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="f2fe5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="f2fe5-103">Usuwa pulę plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="f2fe5-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="f2fe5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2fe5-104">SYNTAX</span></span>

### <span data-ttu-id="f2fe5-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f2fe5-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2fe5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2fe5-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2fe5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2fe5-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2fe5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2fe5-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2fe5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f2fe5-109">DESCRIPTION</span></span>
<span data-ttu-id="f2fe5-110">Polecenie cmdlet **Remove-AzNetAppFilesPool** usuwa pulę ANF.</span><span class="sxs-lookup"><span data-stu-id="f2fe5-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="f2fe5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2fe5-111">EXAMPLES</span></span>

### <span data-ttu-id="f2fe5-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2fe5-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="f2fe5-113">To polecenie usuwa pulę ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="f2fe5-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="f2fe5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2fe5-114">PARAMETERS</span></span>

### <span data-ttu-id="f2fe5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2fe5-115">-AccountName</span></span>
<span data-ttu-id="f2fe5-116">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="f2fe5-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f2fe5-117">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="f2fe5-117">-AccountObject</span></span>
<span data-ttu-id="f2fe5-118">Obiekt konta zawierający pulę do usunięcia</span><span class="sxs-lookup"><span data-stu-id="f2fe5-118">The account object containing the pool to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fe5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2fe5-119">-DefaultProfile</span></span>
<span data-ttu-id="f2fe5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2fe5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2fe5-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f2fe5-121">-InputObject</span></span>
<span data-ttu-id="f2fe5-122">Obiekt puli do usunięcia</span><span class="sxs-lookup"><span data-stu-id="f2fe5-122">The pool object to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fe5-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2fe5-123">-Name</span></span>
<span data-ttu-id="f2fe5-124">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="f2fe5-124">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2fe5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2fe5-125">-PassThru</span></span>
<span data-ttu-id="f2fe5-126">Zwraca, czy określona pula została pomyślnie usunięta.</span><span class="sxs-lookup"><span data-stu-id="f2fe5-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="f2fe5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2fe5-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2fe5-128">Grupa zasobów puli ANF</span><span class="sxs-lookup"><span data-stu-id="f2fe5-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="f2fe5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2fe5-129">-ResourceId</span></span>
<span data-ttu-id="f2fe5-130">Identyfikator zasobu puli ANF</span><span class="sxs-lookup"><span data-stu-id="f2fe5-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="f2fe5-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2fe5-131">-Confirm</span></span>
<span data-ttu-id="f2fe5-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2fe5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2fe5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2fe5-133">-WhatIf</span></span>
<span data-ttu-id="f2fe5-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2fe5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2fe5-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2fe5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2fe5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2fe5-136">CommonParameters</span></span>
<span data-ttu-id="f2fe5-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2fe5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f2fe5-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2fe5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2fe5-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2fe5-139">INPUTS</span></span>

### <span data-ttu-id="f2fe5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f2fe5-140">System.String</span></span>

### <span data-ttu-id="f2fe5-141">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f2fe5-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="f2fe5-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f2fe5-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="f2fe5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2fe5-143">OUTPUTS</span></span>

### <span data-ttu-id="f2fe5-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2fe5-144">System.Boolean</span></span>

## <span data-ttu-id="f2fe5-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2fe5-145">NOTES</span></span>

## <span data-ttu-id="f2fe5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2fe5-146">RELATED LINKS</span></span>
