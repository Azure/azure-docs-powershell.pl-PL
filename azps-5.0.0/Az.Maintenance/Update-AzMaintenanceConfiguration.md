---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231819"
---
# <span data-ttu-id="8efae-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8efae-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="8efae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8efae-102">SYNOPSIS</span></span>
<span data-ttu-id="8efae-103">Rekord konfiguracji poprawki</span><span class="sxs-lookup"><span data-stu-id="8efae-103">Patch configuration record</span></span>

## <span data-ttu-id="8efae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8efae-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8efae-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8efae-105">DESCRIPTION</span></span>
<span data-ttu-id="8efae-106">Rekord konfiguracji konserwacja poprawki</span><span class="sxs-lookup"><span data-stu-id="8efae-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="8efae-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8efae-107">EXAMPLES</span></span>

### <span data-ttu-id="8efae-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8efae-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="8efae-109">Rekord konfiguracji konserwacja poprawki</span><span class="sxs-lookup"><span data-stu-id="8efae-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="8efae-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8efae-110">PARAMETERS</span></span>

### <span data-ttu-id="8efae-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8efae-111">-AsJob</span></span>
<span data-ttu-id="8efae-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8efae-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8efae-113">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="8efae-113">-Configuration</span></span>
<span data-ttu-id="8efae-114">Konfiguracja konserwacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="8efae-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8efae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8efae-115">-DefaultProfile</span></span>
<span data-ttu-id="8efae-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8efae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8efae-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8efae-117">-Name</span></span>
<span data-ttu-id="8efae-118">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="8efae-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="8efae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8efae-119">-ResourceGroupName</span></span>
<span data-ttu-id="8efae-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8efae-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="8efae-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8efae-121">-Confirm</span></span>
<span data-ttu-id="8efae-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8efae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8efae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8efae-123">-WhatIf</span></span>
<span data-ttu-id="8efae-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8efae-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8efae-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8efae-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8efae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8efae-126">CommonParameters</span></span>
<span data-ttu-id="8efae-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8efae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8efae-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8efae-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8efae-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8efae-129">INPUTS</span></span>

### <span data-ttu-id="8efae-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8efae-130">System.String</span></span>

### <span data-ttu-id="8efae-131">Microsoft. Azure. Commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8efae-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="8efae-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8efae-132">OUTPUTS</span></span>

### <span data-ttu-id="8efae-133">Microsoft. Azure. Commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8efae-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="8efae-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8efae-134">NOTES</span></span>

## <span data-ttu-id="8efae-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8efae-135">RELATED LINKS</span></span>
