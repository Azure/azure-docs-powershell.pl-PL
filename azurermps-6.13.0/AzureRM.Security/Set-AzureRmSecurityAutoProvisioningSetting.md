---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: e99ead17cad0a3c6c440967ec1b1852bb5568a26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717050"
---
# <span data-ttu-id="79d8c-101">Set-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="79d8c-101">Set-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="79d8c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="79d8c-103">Aktualizowanie ustawienia automatycznego dostarczania</span><span class="sxs-lookup"><span data-stu-id="79d8c-103">Updates automatic provisioning setting</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79d8c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79d8c-104">SYNTAX</span></span>

### <span data-ttu-id="79d8c-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79d8c-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79d8c-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="79d8c-106">ResourceId</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79d8c-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="79d8c-107">InputObject</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79d8c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="79d8c-108">DESCRIPTION</span></span>
<span data-ttu-id="79d8c-109">Włącza lub wyłącza automatyczne ustawienia inicjowania obsługi dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="79d8c-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="79d8c-110">Ustawienia automatycznego inicjowania obsługi pozwalają zdecydować, czy usługa Azure Security Center ma automatycznie zastrzec Agent zabezpieczeń, który zostanie zainstalowany na maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="79d8c-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="79d8c-111">Agent zabezpieczeń będzie monitorował swoją maszynę wirtualną, aby utworzyć alerty zabezpieczeń i monitorować zgodność z zabezpieczeniami maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="79d8c-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="79d8c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79d8c-112">EXAMPLES</span></span>

### <span data-ttu-id="79d8c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79d8c-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="79d8c-114">Włącza automatyczne ustawianie inicjowania obsługi dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="79d8c-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="79d8c-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="79d8c-115">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="79d8c-116">Wyłącza automatyczne ustawianie inicjowania obsługi dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="79d8c-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="79d8c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79d8c-117">PARAMETERS</span></span>

### <span data-ttu-id="79d8c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d8c-118">-DefaultProfile</span></span>
<span data-ttu-id="79d8c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79d8c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d8c-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="79d8c-120">-EnableAutoProvision</span></span>
<span data-ttu-id="79d8c-121">Automatyczne Inicjowanie obsługi.</span><span class="sxs-lookup"><span data-stu-id="79d8c-121">Automatic Provisioning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d8c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="79d8c-122">-InputObject</span></span>
<span data-ttu-id="79d8c-123">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="79d8c-123">Input Object.</span></span>

```yaml
Type: PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79d8c-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79d8c-124">-Name</span></span>
<span data-ttu-id="79d8c-125">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="79d8c-125">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d8c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79d8c-126">-ResourceId</span></span>
<span data-ttu-id="79d8c-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="79d8c-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79d8c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79d8c-128">-Confirm</span></span>
<span data-ttu-id="79d8c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79d8c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d8c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79d8c-130">-WhatIf</span></span>
<span data-ttu-id="79d8c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79d8c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79d8c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79d8c-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d8c-133">CommonParameters</span></span>
<span data-ttu-id="79d8c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79d8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d8c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79d8c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d8c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79d8c-136">INPUTS</span></span>

### <span data-ttu-id="79d8c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="79d8c-137">System.String</span></span>
<span data-ttu-id="79d8c-138">System. Management. Automation. SwitchParameter Microsoft. Azure. Commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="79d8c-138">System.Management.Automation.SwitchParameter Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="79d8c-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79d8c-139">OUTPUTS</span></span>

### <span data-ttu-id="79d8c-140">Microsoft. Azure. Commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="79d8c-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="79d8c-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79d8c-141">NOTES</span></span>

## <span data-ttu-id="79d8c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79d8c-142">RELATED LINKS</span></span>
