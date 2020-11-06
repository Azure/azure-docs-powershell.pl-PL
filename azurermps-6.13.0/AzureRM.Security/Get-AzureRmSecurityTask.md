---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityTask.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityTask.md
ms.openlocfilehash: 51c2772a891cf39ba780c6ff3da0af40170f477e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526038"
---
# <span data-ttu-id="2db45-101">Get-AzureRmSecurityTask</span><span class="sxs-lookup"><span data-stu-id="2db45-101">Get-AzureRmSecurityTask</span></span>

## <span data-ttu-id="2db45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2db45-102">SYNOPSIS</span></span>
<span data-ttu-id="2db45-103">Pobiera zadania związane z zabezpieczeniami, w których usługa Azure Security Center zaleca wykonywanie zadań w celu wzmocnienia Posture zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="2db45-103">Gets the security tasks that Azure Security Center recommends you to do in order to strengthen your security posture.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2db45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2db45-104">SYNTAX</span></span>

### <span data-ttu-id="2db45-105">SubscriptionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2db45-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityTask [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db45-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="2db45-106">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityTask -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2db45-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="2db45-107">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityTask -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2db45-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2db45-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityTask -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2db45-109">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2db45-109">ResourceId</span></span>
```
Get-AzureRmSecurityTask -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2db45-110">Opis</span><span class="sxs-lookup"><span data-stu-id="2db45-110">DESCRIPTION</span></span>
<span data-ttu-id="2db45-111">Usługa Azure Security Center umożliwia skanowanie zasobów w celu wykrywania potencjalnych problemów z zabezpieczeniami.</span><span class="sxs-lookup"><span data-stu-id="2db45-111">Azure Security Center scans your resources to detect potential security issues.</span></span>
<span data-ttu-id="2db45-112">To polecenie cmdlet umożliwia odnajdowanie zadań związanych z zabezpieczeniami, które program Azure Security Center poleca.</span><span class="sxs-lookup"><span data-stu-id="2db45-112">This cmdlet lets you discover the security tasks that Azure Security Center recommends you to do.</span></span>

## <span data-ttu-id="2db45-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2db45-113">EXAMPLES</span></span>

### <span data-ttu-id="2db45-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2db45-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityTask
Id                                                                                                                                              Name                                 RecommendationType                                  ResourceId
--                                                                                                                                              ----                                 ------------------                                  ----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/08357a1e-c534-756f-cbb9-7b45e73f3137 08357a1e-c534-756f-cbb9-7b45e73f3137 Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/0876feac-8c60-3fef-d95e-2c43b333ff14 0876feac-8c60-3fef-d95e-2c43b333ff14 Antimalware Health Issues                           /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/09ea0fa9-ce5a-d703-e17b-08f1d5246e2c 09ea0fa9-ce5a-d703-e17b-08f1d5246e2c Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/11ff8541-820e-cecc-75de-91be7c0d8419 11ff8541-820e-cecc-75de-91be7c0d8419 Subscription has machines with failed baseline rule /subscriptions/48...
```

<span data-ttu-id="2db45-115">Pobiera wszystkie zadania związane z zabezpieczeniami, które zostały wykryte dla zasobów w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="2db45-115">Gets all the security tasks that were discovered on resources inside a subscription.</span></span>

### <span data-ttu-id="2db45-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2db45-116">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityTask -ResourceGroupName "myService1"

Id                                                                                                                                                                        Name                                 RecommendationType                   ResourceI
                                                                                                                                                                                                                                                    d        
--                                                                                                                                                                        ----                                 ------------------                   ---------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/47f736fa-0ec8-a372-de49-8cf18527930c 47f736fa-0ec8-a372-de49-8cf18527930c ConfigureTier2Waf                    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/5696e90f-833d-494c-8833-f3be335fa9cb 5696e90f-833d-494c-8833-f3be335fa9cb NetworkSecurityGroupMissingOnVm      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/65193cce-25a1-b30f-f94e-69d52e22923c 65193cce-25a1-b30f-f94e-69d52e22923c VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/7e28a40d-e746-4751-8340-5126d6b77ae5 7e28a40d-e746-4751-8340-5126d6b77ae5 NetworkSecurityGroupMissingOnSubnet  /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/94867597-75e5-cfb6-8b71-e5e5253a24e1 94867597-75e5-cfb6-8b71-e5e5253a24e1 EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/a02fffd5-1956-a6d7-73da-a87a65ae02f4 a02fffd5-1956-a6d7-73da-a87a65ae02f4 VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/bd382d04-b478-ac77-e89f-300789032367 bd382d04-b478-ac77-e89f-300789032367 ProvisionNgfw                        /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/ce43626a-d56b-6a38-49ef-3ad7a731666e ce43626a-d56b-6a38-49ef-3ad7a731666e EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/dcfb6365-799e-5ed4-f344-d86a0a4c2992 dcfb6365-799e-5ed4-f344-d86a0a4c2992 Enable auditing for the SQL database /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/ed736ed1-3f42-a95a-0b9e-458c44233937 ed736ed1-3f42-a95a-0b9e-458c44233937 Enable auditing for the SQL server   /subsc...
```

<span data-ttu-id="2db45-117">Pobiera wszystkie zadania związane z zabezpieczeniami, które zostały wykryte dla zasobów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2db45-117">Gets all the security tasks that were discovered on resources inside a resource group.</span></span>

### <span data-ttu-id="2db45-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2db45-118">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmSecurityTask -ResourceGroupName "myService1" -Name "22ef553d-f13a-5227-ee4c-7cc861d28c96"

Id                                                                                                                                                                        Name                                 RecommendationType              ResourceId    
--                                                                                                                                                                        ----                                 ------------------              ----------    
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard /subscripti...
```

<span data-ttu-id="2db45-119">Pobiera określone zadanie zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="2db45-119">Gets a specific security task.</span></span>

## <span data-ttu-id="2db45-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2db45-120">PARAMETERS</span></span>

### <span data-ttu-id="2db45-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db45-121">-DefaultProfile</span></span>
<span data-ttu-id="2db45-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2db45-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2db45-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2db45-123">-Name</span></span>
<span data-ttu-id="2db45-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="2db45-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db45-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db45-125">-ResourceGroupName</span></span>
<span data-ttu-id="2db45-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2db45-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2db45-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2db45-127">-ResourceId</span></span>
<span data-ttu-id="2db45-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2db45-128">Resource ID.</span></span>

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

### <span data-ttu-id="2db45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db45-129">CommonParameters</span></span>
<span data-ttu-id="2db45-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2db45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db45-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2db45-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db45-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2db45-132">INPUTS</span></span>

### <span data-ttu-id="2db45-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2db45-133">System.String</span></span>

## <span data-ttu-id="2db45-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2db45-134">OUTPUTS</span></span>

### <span data-ttu-id="2db45-135">Microsoft. Azure. Commands. Security. models. Tasks. PSSecurityTask</span><span class="sxs-lookup"><span data-stu-id="2db45-135">Microsoft.Azure.Commands.Security.Models.Tasks.PSSecurityTask</span></span>

## <span data-ttu-id="2db45-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2db45-136">NOTES</span></span>

## <span data-ttu-id="2db45-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2db45-137">RELATED LINKS</span></span>
