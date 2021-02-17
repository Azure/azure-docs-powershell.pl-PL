---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 04454028957dfee3c7d50c47341be7e979ed3a9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194555"
---
# <span data-ttu-id="a6fbc-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="a6fbc-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="a6fbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="a6fbc-103">Usuwa ustawienie synchronizacji</span><span class="sxs-lookup"><span data-stu-id="a6fbc-103">removes a synchronization setting</span></span>

## <span data-ttu-id="a6fbc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6fbc-104">SYNTAX</span></span>

### <span data-ttu-id="a6fbc-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a6fbc-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a6fbc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6fbc-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6fbc-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6fbc-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6fbc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6fbc-108">DESCRIPTION</span></span>
<span data-ttu-id="a6fbc-109">Polecenie **cmdlet Remove-AzDataShareSynchronizationSetting** usuwa ustawienie synchronizacji udostępniania danych</span><span class="sxs-lookup"><span data-stu-id="a6fbc-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="a6fbc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6fbc-110">EXAMPLES</span></span>

### <span data-ttu-id="a6fbc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a6fbc-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a6fbc-112">Te polecenia usuwają ustawienie synchronizacji o nazwie AdsShareSynchronizationSetting z usługi Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="a6fbc-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="a6fbc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6fbc-113">PARAMETERS</span></span>

### <span data-ttu-id="a6fbc-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a6fbc-114">-AccountName</span></span>
<span data-ttu-id="a6fbc-115">Nazwa konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="a6fbc-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="a6fbc-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a6fbc-116">-AsJob</span></span>
<span data-ttu-id="a6fbc-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="a6fbc-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="a6fbc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6fbc-118">-DefaultProfile</span></span>
<span data-ttu-id="a6fbc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6fbc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6fbc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6fbc-120">-InputObject</span></span>
<span data-ttu-id="a6fbc-121">Ustawienie synchronizacji udostępniania danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6fbc-121">The Azure Data Share Synchronization setting.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6fbc-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a6fbc-122">-Name</span></span>
<span data-ttu-id="a6fbc-123">Nazwa ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="a6fbc-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="a6fbc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6fbc-124">-PassThru</span></span>
<span data-ttu-id="a6fbc-125">Zwracany obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="a6fbc-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="a6fbc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6fbc-126">-ResourceGroupName</span></span>
<span data-ttu-id="a6fbc-127">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="a6fbc-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a6fbc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6fbc-128">-ResourceId</span></span>
<span data-ttu-id="a6fbc-129">Identyfikator zasobu ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="a6fbc-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="a6fbc-130">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a6fbc-130">-ShareName</span></span>
<span data-ttu-id="a6fbc-131">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a6fbc-131">Azure data share name</span></span>

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

### <span data-ttu-id="a6fbc-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6fbc-132">-Confirm</span></span>
<span data-ttu-id="a6fbc-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a6fbc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6fbc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6fbc-134">-WhatIf</span></span>
<span data-ttu-id="a6fbc-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6fbc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6fbc-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a6fbc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6fbc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6fbc-137">CommonParameters</span></span>
<span data-ttu-id="a6fbc-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6fbc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6fbc-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6fbc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6fbc-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6fbc-140">INPUTS</span></span>

### <span data-ttu-id="a6fbc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a6fbc-141">System.String</span></span>

### <span data-ttu-id="a6fbc-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="a6fbc-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="a6fbc-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6fbc-143">OUTPUTS</span></span>

### <span data-ttu-id="a6fbc-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6fbc-144">System.Boolean</span></span>

## <span data-ttu-id="a6fbc-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6fbc-145">NOTES</span></span>

## <span data-ttu-id="a6fbc-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6fbc-146">RELATED LINKS</span></span>
