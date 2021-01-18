---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503002"
---
# <span data-ttu-id="04ad9-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="04ad9-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="04ad9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="04ad9-103">Aktualizowanie ustawienia zabezpieczeń w centrum zabezpieczeń platformy Azure</span><span class="sxs-lookup"><span data-stu-id="04ad9-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="04ad9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04ad9-104">SYNTAX</span></span>

### <span data-ttu-id="04ad9-105">GeneralScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="04ad9-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ad9-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="04ad9-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ad9-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="04ad9-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ad9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="04ad9-108">DESCRIPTION</span></span>
<span data-ttu-id="04ad9-109">Polecenie cmdlet Set-AzSecuritySetting aktualizuje określone ustawienie zabezpieczeń w usłudze Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="04ad9-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="04ad9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04ad9-110">EXAMPLES</span></span>

### <span data-ttu-id="04ad9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="04ad9-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="04ad9-112">Aktualizowanie ustawienia eksportu danych MCAS</span><span class="sxs-lookup"><span data-stu-id="04ad9-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="04ad9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04ad9-113">PARAMETERS</span></span>

### <span data-ttu-id="04ad9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ad9-114">-DefaultProfile</span></span>
<span data-ttu-id="04ad9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04ad9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04ad9-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="04ad9-116">-Enabled</span></span>
<span data-ttu-id="04ad9-117">Włącza ustawienie.</span><span class="sxs-lookup"><span data-stu-id="04ad9-117">Enables the setting.</span></span>

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

### <span data-ttu-id="04ad9-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="04ad9-118">-InputObject</span></span>
<span data-ttu-id="04ad9-119">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="04ad9-119">Input Object.</span></span>

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

### <span data-ttu-id="04ad9-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="04ad9-120">-SettingKind</span></span>
<span data-ttu-id="04ad9-121">Rodzaj ustawienia.</span><span class="sxs-lookup"><span data-stu-id="04ad9-121">Setting kind.</span></span> <span data-ttu-id="04ad9-122">(DataExportSettings)</span><span class="sxs-lookup"><span data-stu-id="04ad9-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="04ad9-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="04ad9-123">-SettingName</span></span>
<span data-ttu-id="04ad9-124">Nazwa ustawienia.</span><span class="sxs-lookup"><span data-stu-id="04ad9-124">Setting name.</span></span> <span data-ttu-id="04ad9-125">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="04ad9-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="04ad9-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04ad9-126">-Confirm</span></span>
<span data-ttu-id="04ad9-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04ad9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ad9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ad9-128">-WhatIf</span></span>
<span data-ttu-id="04ad9-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04ad9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04ad9-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04ad9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ad9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ad9-131">CommonParameters</span></span>
<span data-ttu-id="04ad9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ad9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ad9-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04ad9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ad9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04ad9-134">INPUTS</span></span>

### <span data-ttu-id="04ad9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="04ad9-135">System.String</span></span>
### <span data-ttu-id="04ad9-136">Microsoft. Azure. Commands. Security. MODELES. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="04ad9-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="04ad9-137">Microsoft. Azure. Commands. Security. MODELES. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="04ad9-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="04ad9-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04ad9-138">System.Boolean</span></span>

## <span data-ttu-id="04ad9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04ad9-139">OUTPUTS</span></span>

### <span data-ttu-id="04ad9-140">Microsoft. Azure. Commands. Security. MODELES. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="04ad9-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="04ad9-141">Microsoft. Azure. Commands. Security. MODELES. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="04ad9-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="04ad9-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04ad9-142">NOTES</span></span>

## <span data-ttu-id="04ad9-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04ad9-143">RELATED LINKS</span></span>
