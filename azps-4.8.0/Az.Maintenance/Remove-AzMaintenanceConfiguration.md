---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220605"
---
# <span data-ttu-id="507da-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="507da-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="507da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="507da-102">SYNOPSIS</span></span>
<span data-ttu-id="507da-103">Usuwanie rekordu konfiguracji</span><span class="sxs-lookup"><span data-stu-id="507da-103">Delete Configuration record</span></span>

## <span data-ttu-id="507da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="507da-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="507da-105">Opis</span><span class="sxs-lookup"><span data-stu-id="507da-105">DESCRIPTION</span></span>
<span data-ttu-id="507da-106">Usuwanie rekordu konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="507da-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="507da-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="507da-107">EXAMPLES</span></span>

### <span data-ttu-id="507da-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="507da-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="507da-109">Usuwanie rekordu konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="507da-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="507da-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="507da-110">PARAMETERS</span></span>

### <span data-ttu-id="507da-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="507da-111">-AsJob</span></span>
<span data-ttu-id="507da-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="507da-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="507da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="507da-113">-DefaultProfile</span></span>
<span data-ttu-id="507da-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="507da-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="507da-115">-Force</span><span class="sxs-lookup"><span data-stu-id="507da-115">-Force</span></span>
<span data-ttu-id="507da-116">Wymuszaj usunięcie bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="507da-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="507da-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="507da-117">-Name</span></span>
<span data-ttu-id="507da-118">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="507da-118">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="507da-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="507da-119">-PassThru</span></span>
<span data-ttu-id="507da-120">Zwraca stan operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="507da-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="507da-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="507da-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="507da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="507da-122">-ResourceGroupName</span></span>
<span data-ttu-id="507da-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="507da-123">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="507da-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="507da-124">-Confirm</span></span>
<span data-ttu-id="507da-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="507da-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="507da-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="507da-126">-WhatIf</span></span>
<span data-ttu-id="507da-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="507da-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="507da-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="507da-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="507da-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="507da-129">CommonParameters</span></span>
<span data-ttu-id="507da-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="507da-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="507da-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="507da-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="507da-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="507da-132">INPUTS</span></span>

### <span data-ttu-id="507da-133">System. String</span><span class="sxs-lookup"><span data-stu-id="507da-133">System.String</span></span>

## <span data-ttu-id="507da-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="507da-134">OUTPUTS</span></span>

### <span data-ttu-id="507da-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="507da-135">System.Boolean</span></span>

## <span data-ttu-id="507da-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="507da-136">NOTES</span></span>

## <span data-ttu-id="507da-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="507da-137">RELATED LINKS</span></span>
