---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232470"
---
# <span data-ttu-id="ad19e-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="ad19e-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="ad19e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad19e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad19e-103">Aktualizowanie ustawienia automatycznego dostarczania</span><span class="sxs-lookup"><span data-stu-id="ad19e-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="ad19e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad19e-104">SYNTAX</span></span>

### <span data-ttu-id="ad19e-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ad19e-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad19e-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="ad19e-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad19e-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="ad19e-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad19e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ad19e-108">DESCRIPTION</span></span>
<span data-ttu-id="ad19e-109">Włącza lub wyłącza automatyczne ustawienia inicjowania obsługi dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ad19e-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="ad19e-110">Ustawienia automatycznego inicjowania obsługi pozwalają zdecydować, czy usługa Azure Security Center ma automatycznie zastrzec Agent zabezpieczeń, który zostanie zainstalowany na maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="ad19e-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="ad19e-111">Agent zabezpieczeń będzie monitorował swoją maszynę wirtualną, aby utworzyć alerty zabezpieczeń i monitorować zgodność z zabezpieczeniami maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ad19e-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="ad19e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad19e-112">EXAMPLES</span></span>

### <span data-ttu-id="ad19e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad19e-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="ad19e-114">Włącza automatyczne ustawianie inicjowania obsługi dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ad19e-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="ad19e-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ad19e-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="ad19e-116">Wyłącza automatyczne ustawianie inicjowania obsługi dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ad19e-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="ad19e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad19e-117">PARAMETERS</span></span>

### <span data-ttu-id="ad19e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad19e-118">-DefaultProfile</span></span>
<span data-ttu-id="ad19e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad19e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad19e-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="ad19e-120">-EnableAutoProvision</span></span>
<span data-ttu-id="ad19e-121">Automatyczne Inicjowanie obsługi.</span><span class="sxs-lookup"><span data-stu-id="ad19e-121">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="ad19e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ad19e-122">-InputObject</span></span>
<span data-ttu-id="ad19e-123">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="ad19e-123">Input Object.</span></span>

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

### <span data-ttu-id="ad19e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad19e-124">-Name</span></span>
<span data-ttu-id="ad19e-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ad19e-125">Resource name.</span></span>

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

### <span data-ttu-id="ad19e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad19e-126">-ResourceId</span></span>
<span data-ttu-id="ad19e-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ad19e-127">Resource ID.</span></span>

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

### <span data-ttu-id="ad19e-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad19e-128">-Confirm</span></span>
<span data-ttu-id="ad19e-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad19e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad19e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad19e-130">-WhatIf</span></span>
<span data-ttu-id="ad19e-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad19e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad19e-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad19e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad19e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad19e-133">CommonParameters</span></span>
<span data-ttu-id="ad19e-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad19e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad19e-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad19e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad19e-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad19e-136">INPUTS</span></span>

### <span data-ttu-id="ad19e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ad19e-137">System.String</span></span>

### <span data-ttu-id="ad19e-138">Microsoft. Azure. Commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="ad19e-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="ad19e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad19e-139">OUTPUTS</span></span>

### <span data-ttu-id="ad19e-140">Microsoft. Azure. Commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="ad19e-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="ad19e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad19e-141">NOTES</span></span>

## <span data-ttu-id="ad19e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad19e-142">RELATED LINKS</span></span>
