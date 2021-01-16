---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 0e8c3fac1c286845686d158c01217b0d4199639c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355282"
---
# <span data-ttu-id="ba044-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="ba044-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="ba044-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba044-102">SYNOPSIS</span></span>
<span data-ttu-id="ba044-103">Usuwanie konta dataudziałowego</span><span class="sxs-lookup"><span data-stu-id="ba044-103">Removes a datashare account</span></span>

## <span data-ttu-id="ba044-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba044-104">SYNTAX</span></span>

### <span data-ttu-id="ba044-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ba044-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba044-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba044-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba044-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba044-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba044-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ba044-108">DESCRIPTION</span></span>
<span data-ttu-id="ba044-109">Polecenie cmdlet **Remove-AzDataShareAccount** usuwa konto dataudział.</span><span class="sxs-lookup"><span data-stu-id="ba044-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="ba044-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba044-110">EXAMPLES</span></span>

### <span data-ttu-id="ba044-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ba044-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="ba044-112">To polecenie usuwa konto dataudziałowe o nazwie WikiADS z grupy zasobów o nazwie ADS.</span><span class="sxs-lookup"><span data-stu-id="ba044-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="ba044-113">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="ba044-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="ba044-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba044-114">PARAMETERS</span></span>

### <span data-ttu-id="ba044-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba044-115">-AsJob</span></span>
<span data-ttu-id="ba044-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="ba044-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="ba044-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba044-117">-DefaultProfile</span></span>
<span data-ttu-id="ba044-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba044-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba044-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ba044-119">-Force</span></span>
<span data-ttu-id="ba044-120">{{Opis siły wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="ba044-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="ba044-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ba044-121">-InputObject</span></span>
<span data-ttu-id="ba044-122">Obiekt konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="ba044-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba044-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ba044-123">-Name</span></span>
<span data-ttu-id="ba044-124">Nazwa konta udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="ba044-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="ba044-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba044-125">-PassThru</span></span>
<span data-ttu-id="ba044-126">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="ba044-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="ba044-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba044-127">-ResourceGroupName</span></span>
<span data-ttu-id="ba044-128">Nazwa grupy zasobów konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="ba044-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="ba044-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba044-129">-ResourceId</span></span>
<span data-ttu-id="ba044-130">Identyfikator zasobu konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="ba044-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="ba044-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba044-131">-Confirm</span></span>
<span data-ttu-id="ba044-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba044-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba044-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba044-133">-WhatIf</span></span>
<span data-ttu-id="ba044-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba044-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba044-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ba044-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba044-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba044-136">CommonParameters</span></span>
<span data-ttu-id="ba044-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba044-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba044-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba044-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba044-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba044-139">INPUTS</span></span>

### <span data-ttu-id="ba044-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ba044-140">System.String</span></span>

### <span data-ttu-id="ba044-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="ba044-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="ba044-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba044-142">OUTPUTS</span></span>

### <span data-ttu-id="ba044-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba044-143">System.Boolean</span></span>

## <span data-ttu-id="ba044-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba044-144">NOTES</span></span>

## <span data-ttu-id="ba044-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba044-145">RELATED LINKS</span></span>
