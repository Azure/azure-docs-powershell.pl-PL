---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358276"
---
# <span data-ttu-id="4bcc9-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bcc9-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="4bcc9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4bcc9-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcc9-103">Rekord konfiguracji poprawki</span><span class="sxs-lookup"><span data-stu-id="4bcc9-103">Patch configuration record</span></span>

## <span data-ttu-id="4bcc9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4bcc9-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bcc9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4bcc9-105">DESCRIPTION</span></span>
<span data-ttu-id="4bcc9-106">Rekord konfiguracji konserwacja poprawki</span><span class="sxs-lookup"><span data-stu-id="4bcc9-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="4bcc9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4bcc9-107">EXAMPLES</span></span>

### <span data-ttu-id="4bcc9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4bcc9-108">Example 1</span></span>
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

<span data-ttu-id="4bcc9-109">Rekord konfiguracji konserwacja poprawki</span><span class="sxs-lookup"><span data-stu-id="4bcc9-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="4bcc9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4bcc9-110">PARAMETERS</span></span>

### <span data-ttu-id="4bcc9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bcc9-111">-AsJob</span></span>
<span data-ttu-id="4bcc9-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4bcc9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bcc9-113">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="4bcc9-113">-Configuration</span></span>
<span data-ttu-id="4bcc9-114">Konfiguracja konserwacji do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="4bcc9-114">The maintenance configuration to be updated.</span></span>

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

### <span data-ttu-id="4bcc9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcc9-115">-DefaultProfile</span></span>
<span data-ttu-id="4bcc9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4bcc9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bcc9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4bcc9-117">-Name</span></span>
<span data-ttu-id="4bcc9-118">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="4bcc9-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="4bcc9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bcc9-119">-ResourceGroupName</span></span>
<span data-ttu-id="4bcc9-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4bcc9-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="4bcc9-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4bcc9-121">-Confirm</span></span>
<span data-ttu-id="4bcc9-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bcc9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bcc9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bcc9-123">-WhatIf</span></span>
<span data-ttu-id="4bcc9-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bcc9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bcc9-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4bcc9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bcc9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcc9-126">CommonParameters</span></span>
<span data-ttu-id="4bcc9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bcc9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcc9-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bcc9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcc9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bcc9-129">INPUTS</span></span>

### <span data-ttu-id="4bcc9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4bcc9-130">System.String</span></span>

### <span data-ttu-id="4bcc9-131">Microsoft. Azure. Commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bcc9-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="4bcc9-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4bcc9-132">OUTPUTS</span></span>

### <span data-ttu-id="4bcc9-133">Microsoft. Azure. Commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bcc9-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="4bcc9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4bcc9-134">NOTES</span></span>

## <span data-ttu-id="4bcc9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bcc9-135">RELATED LINKS</span></span>
