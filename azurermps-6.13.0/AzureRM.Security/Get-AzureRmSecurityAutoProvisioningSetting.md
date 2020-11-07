---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 98adc5714f4a4abaeca9fe6723b1a56fe1d49fca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718274"
---
# <span data-ttu-id="04910-101">Get-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="04910-101">Get-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="04910-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04910-102">SYNOPSIS</span></span>
<span data-ttu-id="04910-103">Pobiera ustawienia automatycznego dostarczania zabezpieczeń</span><span class="sxs-lookup"><span data-stu-id="04910-103">Gets the security automatic provisioning settings</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04910-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04910-104">SYNTAX</span></span>

### <span data-ttu-id="04910-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="04910-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04910-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="04910-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04910-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="04910-107">ResourceId</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04910-108">Opis</span><span class="sxs-lookup"><span data-stu-id="04910-108">DESCRIPTION</span></span>
<span data-ttu-id="04910-109">Ustawienia automatycznego udostępniania pozwalają zdecydować, czy usługa Azure Security Cetner ma być automatycznie proviosion Agent zabezpieczeń, który zostanie zainstalowany na maszynach wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="04910-109">Automatic Provisioning Settings let you decide whether you want Azure Security Cetner to automatically proviosion a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="04910-110">Agent zabezpieczeń będzie monitorował swoją maszynę wirtualną, aby utworzyć alerty zabezpieczeń i monitorować zgodność z zabezpieczeniami maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="04910-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="04910-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04910-111">EXAMPLES</span></span>

### <span data-ttu-id="04910-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="04910-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="04910-113">Pobiera ustawienie automatycznej obsługi dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="04910-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="04910-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04910-114">PARAMETERS</span></span>

### <span data-ttu-id="04910-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04910-115">-DefaultProfile</span></span>
<span data-ttu-id="04910-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04910-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04910-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="04910-117">-Name</span></span>
<span data-ttu-id="04910-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="04910-118">Resource name.</span></span>

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

### <span data-ttu-id="04910-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04910-119">-ResourceId</span></span>
<span data-ttu-id="04910-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="04910-120">Resource ID.</span></span>

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

### <span data-ttu-id="04910-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04910-121">CommonParameters</span></span>
<span data-ttu-id="04910-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04910-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04910-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04910-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04910-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04910-124">INPUTS</span></span>

### <span data-ttu-id="04910-125">System. String</span><span class="sxs-lookup"><span data-stu-id="04910-125">System.String</span></span>

## <span data-ttu-id="04910-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04910-126">OUTPUTS</span></span>

### <span data-ttu-id="04910-127">Microsoft. Azure. Commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="04910-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="04910-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04910-128">NOTES</span></span>

## <span data-ttu-id="04910-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04910-129">RELATED LINKS</span></span>
