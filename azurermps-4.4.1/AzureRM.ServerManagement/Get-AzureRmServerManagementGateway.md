---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 6b98f4266e730e1cfb60ef51046e6846f24999d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717161"
---
# <span data-ttu-id="6a189-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="6a189-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="6a189-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a189-102">SYNOPSIS</span></span>
<span data-ttu-id="6a189-103">Pobiera jeden lub więcej bram zarządzania serwera.</span><span class="sxs-lookup"><span data-stu-id="6a189-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a189-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a189-104">SYNTAX</span></span>

### <span data-ttu-id="6a189-105">Noparams (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6a189-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a189-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6a189-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a189-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="6a189-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a189-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="6a189-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a189-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6a189-109">DESCRIPTION</span></span>
<span data-ttu-id="6a189-110">Polecenie cmdlet **Get-AzureRmServerManagementGateway umożliwia pobranie** co najmniej jednej bramy zarządzania serwerem Azure.</span><span class="sxs-lookup"><span data-stu-id="6a189-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="6a189-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a189-111">EXAMPLES</span></span>

### <span data-ttu-id="6a189-112">Przykład 1. Uzyskaj wszystkie bramy w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6a189-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="6a189-113">To polecenie pobiera wszystkie bramy zarządzania serwerem w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6a189-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="6a189-114">Przykład 2: uzyskiwanie bram w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="6a189-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="6a189-115">To polecenie pobiera wszystkie bramy zarządzania serwerem należące do grupy zasobów o nazwie Group001.</span><span class="sxs-lookup"><span data-stu-id="6a189-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="6a189-116">Przykład 3: uzyskiwanie wszystkich zainstalowanych wystąpień bramy</span><span class="sxs-lookup"><span data-stu-id="6a189-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="6a189-117">To polecenie pobiera wszystkie wystąpienia bramy zarządzania serwera o nazwie Gateway01 należącej do grupy zasobów o nazwie Group002.</span><span class="sxs-lookup"><span data-stu-id="6a189-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="6a189-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a189-118">PARAMETERS</span></span>

### <span data-ttu-id="6a189-119">-Gateway</span><span class="sxs-lookup"><span data-stu-id="6a189-119">-Gateway</span></span>
<span data-ttu-id="6a189-120">Określa bramę, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a189-120">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="6a189-121">Do wykonania akcji polecenie cmdlet używa parametrów *ResourceGroupName* i *gatewayname* za pośrednictwem określonej bramy.</span><span class="sxs-lookup"><span data-stu-id="6a189-121">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="6a189-122">Po określeniu tego parametru polecenie cmdlet będzie zawierać szczegółowy stan bramy.</span><span class="sxs-lookup"><span data-stu-id="6a189-122">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a189-123">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="6a189-123">-GatewayName</span></span>
<span data-ttu-id="6a189-124">Określa nazwę bramy zarządzania serwera, dla której to polecenie cmdlet pobiera bramę.</span><span class="sxs-lookup"><span data-stu-id="6a189-124">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="6a189-125">Po określeniu parametru *bramaname* to polecenie cmdlet będzie zawierać szczegółowy stan bramy.</span><span class="sxs-lookup"><span data-stu-id="6a189-125">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a189-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a189-126">-ResourceGroupName</span></span>
<span data-ttu-id="6a189-127">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera bramy.</span><span class="sxs-lookup"><span data-stu-id="6a189-127">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: System.String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a189-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a189-128">-DefaultProfile</span></span>
<span data-ttu-id="6a189-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a189-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a189-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a189-130">CommonParameters</span></span>
<span data-ttu-id="6a189-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a189-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a189-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a189-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a189-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a189-133">INPUTS</span></span>

### <span data-ttu-id="6a189-134">Problem</span><span class="sxs-lookup"><span data-stu-id="6a189-134">Gateway</span></span>
<span data-ttu-id="6a189-135">Parametr "brama" akceptuje wartość typu "brama" z procesu</span><span class="sxs-lookup"><span data-stu-id="6a189-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="6a189-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a189-136">OUTPUTS</span></span>

### <span data-ttu-id="6a189-137">Microsoft. Azure. Commands. ServerManagement. model. Gateway</span><span class="sxs-lookup"><span data-stu-id="6a189-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="6a189-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a189-138">NOTES</span></span>
* <span data-ttu-id="6a189-139">Jeśli to polecenie cmdlet jest używane bez parametrów, zwróci wszystkie bramy skojarzone z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="6a189-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="6a189-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a189-140">RELATED LINKS</span></span>

[<span data-ttu-id="6a189-141">Nowe — AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="6a189-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="6a189-142">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="6a189-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


