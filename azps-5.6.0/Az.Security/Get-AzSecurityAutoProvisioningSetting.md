---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: b48222344e9a9fdb958073a658717d1cafa057f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008513"
---
# <span data-ttu-id="5873f-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="5873f-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="5873f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5873f-102">SYNOPSIS</span></span>
<span data-ttu-id="5873f-103">Pobiera ustawienia automatycznego inicjowania obsługi zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="5873f-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="5873f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5873f-104">SYNTAX</span></span>

### <span data-ttu-id="5873f-105">SubscriptionScope (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5873f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5873f-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="5873f-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5873f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5873f-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5873f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5873f-108">DESCRIPTION</span></span>
<span data-ttu-id="5873f-109">Ustawienia automatycznego inicjowania obsługi administracyjnej pozwalają zdecydować, czy usługa Azure Security Center ma automatycznie aprowizować agenta zabezpieczeń, który zostanie zainstalowany na Twoich maszynych wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="5873f-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="5873f-110">Agent zabezpieczeń będzie monitorował maszyny wirtualnej w celu utworzenia alertów zabezpieczeń i monitorowania zgodności zabezpieczeń maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5873f-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="5873f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5873f-111">EXAMPLES</span></span>

### <span data-ttu-id="5873f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5873f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="5873f-113">Pobiera ustawienie automatycznego inicjowania obsługi administracyjnej dla subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5873f-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="5873f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5873f-114">PARAMETERS</span></span>

### <span data-ttu-id="5873f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5873f-115">-DefaultProfile</span></span>
<span data-ttu-id="5873f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5873f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5873f-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5873f-117">-Name</span></span>
<span data-ttu-id="5873f-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5873f-118">Resource name.</span></span>

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

### <span data-ttu-id="5873f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5873f-119">-ResourceId</span></span>
<span data-ttu-id="5873f-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5873f-120">Resource ID.</span></span>

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

### <span data-ttu-id="5873f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5873f-121">CommonParameters</span></span>
<span data-ttu-id="5873f-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5873f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5873f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5873f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5873f-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5873f-124">INPUTS</span></span>

### <span data-ttu-id="5873f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="5873f-125">System.String</span></span>

## <span data-ttu-id="5873f-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5873f-126">OUTPUTS</span></span>

### <span data-ttu-id="5873f-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="5873f-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="5873f-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5873f-128">NOTES</span></span>

## <span data-ttu-id="5873f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5873f-129">RELATED LINKS</span></span>
