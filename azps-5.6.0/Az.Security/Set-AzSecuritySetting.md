---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 5c7e9d80ffd9109cda1f13f74b1febb3b28e10ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005745"
---
# <span data-ttu-id="e249d-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="e249d-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="e249d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e249d-102">SYNOPSIS</span></span>
<span data-ttu-id="e249d-103">Aktualizowanie ustawienia zabezpieczeń w Centrum zabezpieczeń Platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e249d-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="e249d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e249d-104">SYNTAX</span></span>

### <span data-ttu-id="e249d-105">GeneralScope (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e249d-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e249d-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="e249d-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e249d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e249d-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e249d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e249d-108">DESCRIPTION</span></span>
<span data-ttu-id="e249d-109">Polecenie Set-AzSecuritySetting aktualizuje określone ustawienie zabezpieczeń w Centrum zabezpieczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e249d-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="e249d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e249d-110">EXAMPLES</span></span>

### <span data-ttu-id="e249d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e249d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="e249d-112">Aktualizacja ustawienia eksportowania danych mcas</span><span class="sxs-lookup"><span data-stu-id="e249d-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="e249d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e249d-113">PARAMETERS</span></span>

### <span data-ttu-id="e249d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e249d-114">-DefaultProfile</span></span>
<span data-ttu-id="e249d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e249d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e249d-116">— włączone</span><span class="sxs-lookup"><span data-stu-id="e249d-116">-Enabled</span></span>
<span data-ttu-id="e249d-117">Włącza to ustawienie.</span><span class="sxs-lookup"><span data-stu-id="e249d-117">Enables the setting.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e249d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e249d-118">-InputObject</span></span>
<span data-ttu-id="e249d-119">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="e249d-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e249d-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="e249d-120">-SettingKind</span></span>
<span data-ttu-id="e249d-121">Typ ustawienia.</span><span class="sxs-lookup"><span data-stu-id="e249d-121">Setting kind.</span></span> <span data-ttu-id="e249d-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="e249d-122">(DataExportSettings)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e249d-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="e249d-123">-SettingName</span></span>
<span data-ttu-id="e249d-124">Nazwa ustawienia.</span><span class="sxs-lookup"><span data-stu-id="e249d-124">Setting name.</span></span> <span data-ttu-id="e249d-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="e249d-125">(MCAS/WDATP)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e249d-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e249d-126">-Confirm</span></span>
<span data-ttu-id="e249d-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e249d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e249d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e249d-128">-WhatIf</span></span>
<span data-ttu-id="e249d-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e249d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e249d-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e249d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e249d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e249d-131">CommonParameters</span></span>
<span data-ttu-id="e249d-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e249d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e249d-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e249d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e249d-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e249d-134">INPUTS</span></span>

### <span data-ttu-id="e249d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e249d-135">System.String</span></span>
### <span data-ttu-id="e249d-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="e249d-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="e249d-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="e249d-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="e249d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e249d-138">System.Boolean</span></span>

## <span data-ttu-id="e249d-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e249d-139">OUTPUTS</span></span>

### <span data-ttu-id="e249d-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="e249d-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="e249d-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="e249d-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="e249d-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e249d-142">NOTES</span></span>

## <span data-ttu-id="e249d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e249d-143">RELATED LINKS</span></span>
