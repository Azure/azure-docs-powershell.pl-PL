---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 283bc1a14404c842da0ed99e43596984b1559299
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548660"
---
# <span data-ttu-id="3a3d8-101">Get-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="3a3d8-101">Get-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="3a3d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a3d8-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3d8-103">Pobierz zasady WAF</span><span class="sxs-lookup"><span data-stu-id="3a3d8-103">Get WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a3d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a3d8-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a3d8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a3d8-105">DESCRIPTION</span></span>
<span data-ttu-id="3a3d8-106">**AzureRmFrontDoorFireWallPolicy** cmdletGet pobiera zasady WAF w grupie zasobów w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3a3d8-106">The **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="3a3d8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a3d8-107">EXAMPLES</span></span>

### <span data-ttu-id="3a3d8-108">Przykład 1: Uzyskaj zasady WAF o nazwie $Name w $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a3d8-108">Example 1: Get a WAF policy called $Name in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="3a3d8-109">Uzyskaj zasady WAF o nazwie $Name w $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a3d8-109">Get a WAF policy called $Name in $resourceGroup</span></span>

### <span data-ttu-id="3a3d8-110">Przykład 2: Uzyskaj wszystkie zasady WAF w $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a3d8-110">Example 2: Get all WAF policy in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name1}
Name               : {Name1}
Type               :

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name2}
Name               : {Name2}
Type               :
```

<span data-ttu-id="3a3d8-111">Pobierz wszystkie zasady WAF w $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a3d8-111">Get all WAF policy in $resourceGroup</span></span>

## <span data-ttu-id="3a3d8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a3d8-112">PARAMETERS</span></span>

### <span data-ttu-id="3a3d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3d8-113">-DefaultProfile</span></span>
<span data-ttu-id="3a3d8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a3d8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3d8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a3d8-115">-Name</span></span>
<span data-ttu-id="3a3d8-116">Nazwa FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="3a3d8-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3d8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3d8-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a3d8-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a3d8-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3d8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3d8-119">CommonParameters</span></span>
<span data-ttu-id="3a3d8-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a3d8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3d8-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a3d8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3d8-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a3d8-122">INPUTS</span></span>

### <span data-ttu-id="3a3d8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3a3d8-123">System.String</span></span>

## <span data-ttu-id="3a3d8-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a3d8-124">OUTPUTS</span></span>

### <span data-ttu-id="3a3d8-125">Microsoft. Azure. Commands. FrontDoor. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="3a3d8-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="3a3d8-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a3d8-126">NOTES</span></span>

## <span data-ttu-id="3a3d8-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a3d8-127">RELATED LINKS</span></span>

<span data-ttu-id="3a3d8-128">[Nowe — AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="3a3d8-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span></span>
