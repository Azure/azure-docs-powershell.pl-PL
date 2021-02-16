---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183579"
---
# <span data-ttu-id="f21e9-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="f21e9-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="f21e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f21e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f21e9-103">Aktualizacja ustawienia automatycznego inicjowania obsługi</span><span class="sxs-lookup"><span data-stu-id="f21e9-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="f21e9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f21e9-104">SYNTAX</span></span>

### <span data-ttu-id="f21e9-105">SubscriptionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f21e9-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f21e9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f21e9-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f21e9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f21e9-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f21e9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f21e9-108">DESCRIPTION</span></span>
<span data-ttu-id="f21e9-109">Włącza lub wyłącza ustawienia automatycznego inicjowania obsługi dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f21e9-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="f21e9-110">Ustawienia automatycznego inicjowania obsługi administracyjnej pozwalają zdecydować, czy usługa Azure Security Center ma automatycznie aprowizować agenta zabezpieczeń, który zostanie zainstalowany na Twoich maszynych wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="f21e9-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="f21e9-111">Agent zabezpieczeń będzie monitorował maszyny wirtualnej w celu utworzenia alertów zabezpieczeń i monitorowania zgodności zabezpieczeń maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f21e9-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="f21e9-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f21e9-112">EXAMPLES</span></span>

### <span data-ttu-id="f21e9-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f21e9-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="f21e9-114">Włącza ustawienie automatycznego inicjowania obsługi dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f21e9-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="f21e9-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f21e9-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="f21e9-116">Wyłącza ustawienie automatycznego inicjowania obsługi dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f21e9-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="f21e9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f21e9-117">PARAMETERS</span></span>

### <span data-ttu-id="f21e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f21e9-118">-DefaultProfile</span></span>
<span data-ttu-id="f21e9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f21e9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f21e9-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="f21e9-120">-EnableAutoProvision</span></span>
<span data-ttu-id="f21e9-121">Automatyczne inicjowanie obsługi administracyjnej.</span><span class="sxs-lookup"><span data-stu-id="f21e9-121">Automatic Provisioning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21e9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f21e9-122">-InputObject</span></span>
<span data-ttu-id="f21e9-123">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="f21e9-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f21e9-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f21e9-124">-Name</span></span>
<span data-ttu-id="f21e9-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f21e9-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21e9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f21e9-126">-ResourceId</span></span>
<span data-ttu-id="f21e9-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f21e9-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f21e9-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f21e9-128">-Confirm</span></span>
<span data-ttu-id="f21e9-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f21e9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f21e9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f21e9-130">-WhatIf</span></span>
<span data-ttu-id="f21e9-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f21e9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f21e9-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f21e9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f21e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f21e9-133">CommonParameters</span></span>
<span data-ttu-id="f21e9-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f21e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f21e9-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f21e9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f21e9-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f21e9-136">INPUTS</span></span>

### <span data-ttu-id="f21e9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f21e9-137">System.String</span></span>

### <span data-ttu-id="f21e9-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="f21e9-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="f21e9-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f21e9-139">OUTPUTS</span></span>

### <span data-ttu-id="f21e9-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="f21e9-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="f21e9-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f21e9-141">NOTES</span></span>

## <span data-ttu-id="f21e9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f21e9-142">RELATED LINKS</span></span>
