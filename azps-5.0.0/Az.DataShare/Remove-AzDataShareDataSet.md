---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305160"
---
# <span data-ttu-id="511da-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="511da-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="511da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="511da-102">SYNOPSIS</span></span>
<span data-ttu-id="511da-103">Usuwa mapowanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="511da-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="511da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="511da-104">SYNTAX</span></span>

### <span data-ttu-id="511da-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="511da-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="511da-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="511da-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="511da-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="511da-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="511da-108">Opis</span><span class="sxs-lookup"><span data-stu-id="511da-108">DESCRIPTION</span></span>
<span data-ttu-id="511da-109">Polecenie cmdlet **Remove-AzDataShareDataSet** umożliwia usunięcie zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="511da-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="511da-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="511da-110">EXAMPLES</span></span>

### <span data-ttu-id="511da-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="511da-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="511da-112">To polecenie usuwa zestaw danych o nazwie DS z WikiAds udostępniania.</span><span class="sxs-lookup"><span data-stu-id="511da-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="511da-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="511da-113">PARAMETERS</span></span>

### <span data-ttu-id="511da-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="511da-114">-AccountName</span></span>
<span data-ttu-id="511da-115">Nazwa konta udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="511da-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="511da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511da-116">-DefaultProfile</span></span>
<span data-ttu-id="511da-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="511da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="511da-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="511da-118">-InputObject</span></span>
<span data-ttu-id="511da-119">Obiekt zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="511da-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="511da-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="511da-120">-Name</span></span>
<span data-ttu-id="511da-121">Nazwa zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="511da-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="511da-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="511da-122">-PassThru</span></span>
<span data-ttu-id="511da-123">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="511da-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="511da-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="511da-124">-ResourceGroupName</span></span>
<span data-ttu-id="511da-125">Nazwa grupy zasobów konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="511da-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="511da-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="511da-126">-ResourceId</span></span>
<span data-ttu-id="511da-127">Identyfikator zasobu zestawu danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="511da-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="511da-128">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="511da-128">-ShareName</span></span>
<span data-ttu-id="511da-129">Nazwa udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="511da-129">Azure data share name.</span></span>

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

### <span data-ttu-id="511da-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="511da-130">-Confirm</span></span>
<span data-ttu-id="511da-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="511da-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="511da-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="511da-132">-WhatIf</span></span>
<span data-ttu-id="511da-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="511da-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="511da-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="511da-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="511da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511da-135">CommonParameters</span></span>
<span data-ttu-id="511da-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="511da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511da-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="511da-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511da-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="511da-138">INPUTS</span></span>

### <span data-ttu-id="511da-139">System. String</span><span class="sxs-lookup"><span data-stu-id="511da-139">System.String</span></span>

### <span data-ttu-id="511da-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="511da-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="511da-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="511da-141">OUTPUTS</span></span>

### <span data-ttu-id="511da-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="511da-142">System.Boolean</span></span>

## <span data-ttu-id="511da-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="511da-143">NOTES</span></span>

## <span data-ttu-id="511da-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="511da-144">RELATED LINKS</span></span>
