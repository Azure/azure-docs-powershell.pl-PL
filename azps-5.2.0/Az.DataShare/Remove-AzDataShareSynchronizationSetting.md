---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 04454028957dfee3c7d50c47341be7e979ed3a9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333025"
---
# <span data-ttu-id="10e6e-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="10e6e-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="10e6e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="10e6e-103">Usuwa ustawienie synchronizacji</span><span class="sxs-lookup"><span data-stu-id="10e6e-103">removes a synchronization setting</span></span>

## <span data-ttu-id="10e6e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10e6e-104">SYNTAX</span></span>

### <span data-ttu-id="10e6e-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="10e6e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10e6e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10e6e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10e6e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10e6e-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10e6e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="10e6e-108">DESCRIPTION</span></span>
<span data-ttu-id="10e6e-109">Polecenie cmdlet **Remove-AzDataShareSynchronizationSetting** usuwa ustawienie synchronizacji datashare</span><span class="sxs-lookup"><span data-stu-id="10e6e-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="10e6e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10e6e-110">EXAMPLES</span></span>

### <span data-ttu-id="10e6e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10e6e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="10e6e-112">To polecenie usuwa ustawienie synchronizacji o nazwie AdsShareSynchronizationSetting z AdsShare udostępniania.</span><span class="sxs-lookup"><span data-stu-id="10e6e-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="10e6e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10e6e-113">PARAMETERS</span></span>

### <span data-ttu-id="10e6e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="10e6e-114">-AccountName</span></span>
<span data-ttu-id="10e6e-115">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="10e6e-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="10e6e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10e6e-116">-AsJob</span></span>
<span data-ttu-id="10e6e-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="10e6e-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="10e6e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e6e-118">-DefaultProfile</span></span>
<span data-ttu-id="10e6e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10e6e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10e6e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="10e6e-120">-InputObject</span></span>
<span data-ttu-id="10e6e-121">Ustawienie synchronizacji usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="10e6e-121">The Azure Data Share Synchronization setting.</span></span>


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

### <span data-ttu-id="10e6e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10e6e-122">-Name</span></span>
<span data-ttu-id="10e6e-123">Nazwa ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="10e6e-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="10e6e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10e6e-124">-PassThru</span></span>
<span data-ttu-id="10e6e-125">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="10e6e-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="10e6e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e6e-126">-ResourceGroupName</span></span>
<span data-ttu-id="10e6e-127">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="10e6e-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="10e6e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10e6e-128">-ResourceId</span></span>
<span data-ttu-id="10e6e-129">Identyfikator zasobu Ustawienia synchronizacji</span><span class="sxs-lookup"><span data-stu-id="10e6e-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="10e6e-130">-Nazwa_udziału</span><span class="sxs-lookup"><span data-stu-id="10e6e-130">-ShareName</span></span>
<span data-ttu-id="10e6e-131">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="10e6e-131">Azure data share name</span></span>

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

### <span data-ttu-id="10e6e-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10e6e-132">-Confirm</span></span>
<span data-ttu-id="10e6e-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10e6e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10e6e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e6e-134">-WhatIf</span></span>
<span data-ttu-id="10e6e-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10e6e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10e6e-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10e6e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10e6e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e6e-137">CommonParameters</span></span>
<span data-ttu-id="10e6e-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e6e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e6e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10e6e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e6e-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10e6e-140">INPUTS</span></span>

### <span data-ttu-id="10e6e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="10e6e-141">System.String</span></span>

### <span data-ttu-id="10e6e-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="10e6e-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="10e6e-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10e6e-143">OUTPUTS</span></span>

### <span data-ttu-id="10e6e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10e6e-144">System.Boolean</span></span>

## <span data-ttu-id="10e6e-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10e6e-145">NOTES</span></span>

## <span data-ttu-id="10e6e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10e6e-146">RELATED LINKS</span></span>
