---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183555"
---
# <span data-ttu-id="f30a4-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="f30a4-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="f30a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f30a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f30a4-103">Aktualizowanie ustawienia zabezpieczeń w Centrum zabezpieczeń platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f30a4-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="f30a4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f30a4-104">SYNTAX</span></span>

### <span data-ttu-id="f30a4-105">GeneralScope (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f30a4-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30a4-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="f30a4-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30a4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f30a4-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f30a4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f30a4-108">DESCRIPTION</span></span>
<span data-ttu-id="f30a4-109">Polecenie Set-AzSecuritySetting aktualizuje określone ustawienie zabezpieczeń w Centrum zabezpieczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f30a4-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="f30a4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f30a4-110">EXAMPLES</span></span>

### <span data-ttu-id="f30a4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f30a4-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="f30a4-112">Aktualizacja ustawienia eksportowania danych mcas</span><span class="sxs-lookup"><span data-stu-id="f30a4-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="f30a4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f30a4-113">PARAMETERS</span></span>

### <span data-ttu-id="f30a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30a4-114">-DefaultProfile</span></span>
<span data-ttu-id="f30a4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f30a4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f30a4-116">— włączone</span><span class="sxs-lookup"><span data-stu-id="f30a4-116">-Enabled</span></span>
<span data-ttu-id="f30a4-117">Włącza to ustawienie.</span><span class="sxs-lookup"><span data-stu-id="f30a4-117">Enables the setting.</span></span>

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

### <span data-ttu-id="f30a4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f30a4-118">-InputObject</span></span>
<span data-ttu-id="f30a4-119">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="f30a4-119">Input Object.</span></span>

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

### <span data-ttu-id="f30a4-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="f30a4-120">-SettingKind</span></span>
<span data-ttu-id="f30a4-121">Typ ustawienia.</span><span class="sxs-lookup"><span data-stu-id="f30a4-121">Setting kind.</span></span> <span data-ttu-id="f30a4-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="f30a4-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="f30a4-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="f30a4-123">-SettingName</span></span>
<span data-ttu-id="f30a4-124">Nazwa ustawienia.</span><span class="sxs-lookup"><span data-stu-id="f30a4-124">Setting name.</span></span> <span data-ttu-id="f30a4-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="f30a4-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="f30a4-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f30a4-126">-Confirm</span></span>
<span data-ttu-id="f30a4-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f30a4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f30a4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f30a4-128">-WhatIf</span></span>
<span data-ttu-id="f30a4-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f30a4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f30a4-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f30a4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f30a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30a4-131">CommonParameters</span></span>
<span data-ttu-id="f30a4-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f30a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30a4-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f30a4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30a4-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f30a4-134">INPUTS</span></span>

### <span data-ttu-id="f30a4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f30a4-135">System.String</span></span>
### <span data-ttu-id="f30a4-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="f30a4-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="f30a4-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="f30a4-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="f30a4-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f30a4-138">System.Boolean</span></span>

## <span data-ttu-id="f30a4-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f30a4-139">OUTPUTS</span></span>

### <span data-ttu-id="f30a4-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="f30a4-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="f30a4-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="f30a4-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="f30a4-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f30a4-142">NOTES</span></span>

## <span data-ttu-id="f30a4-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f30a4-143">RELATED LINKS</span></span>
