---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503048"
---
# <span data-ttu-id="b02ef-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="b02ef-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="b02ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b02ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b02ef-103">Pobiera ustawienia automatycznego dostarczania zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="b02ef-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="b02ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b02ef-104">SYNTAX</span></span>

### <span data-ttu-id="b02ef-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b02ef-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b02ef-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b02ef-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b02ef-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="b02ef-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b02ef-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b02ef-108">DESCRIPTION</span></span>
<span data-ttu-id="b02ef-109">Ustawienia automatycznego inicjowania obsługi pozwalają zdecydować, czy usługa Azure Security Center ma automatycznie zastrzec Agent zabezpieczeń, który zostanie zainstalowany na maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="b02ef-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="b02ef-110">Agent zabezpieczeń będzie monitorował swoją maszynę wirtualną, aby utworzyć alerty zabezpieczeń i monitorować zgodność z zabezpieczeniami maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b02ef-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="b02ef-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b02ef-111">EXAMPLES</span></span>

### <span data-ttu-id="b02ef-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b02ef-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="b02ef-113">Pobiera ustawienie automatycznej obsługi dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b02ef-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="b02ef-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b02ef-114">PARAMETERS</span></span>

### <span data-ttu-id="b02ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02ef-115">-DefaultProfile</span></span>
<span data-ttu-id="b02ef-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b02ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b02ef-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b02ef-117">-Name</span></span>
<span data-ttu-id="b02ef-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="b02ef-118">Resource name.</span></span>

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

### <span data-ttu-id="b02ef-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b02ef-119">-ResourceId</span></span>
<span data-ttu-id="b02ef-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b02ef-120">Resource ID.</span></span>

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

### <span data-ttu-id="b02ef-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02ef-121">CommonParameters</span></span>
<span data-ttu-id="b02ef-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b02ef-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02ef-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b02ef-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02ef-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b02ef-124">INPUTS</span></span>

### <span data-ttu-id="b02ef-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b02ef-125">System.String</span></span>

## <span data-ttu-id="b02ef-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b02ef-126">OUTPUTS</span></span>

### <span data-ttu-id="b02ef-127">Microsoft. Azure. Commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="b02ef-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="b02ef-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b02ef-128">NOTES</span></span>

## <span data-ttu-id="b02ef-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b02ef-129">RELATED LINKS</span></span>
