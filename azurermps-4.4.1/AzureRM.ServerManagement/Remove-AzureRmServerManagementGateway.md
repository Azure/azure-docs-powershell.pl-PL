---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 41F8F851-6F9F-4DA4-8CE6-D8C9B7CF68D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
ms.openlocfilehash: 2bcfac139d38f0b6f7d621a7761ce01d1d3f2f45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546023"
---
# <span data-ttu-id="19525-101">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="19525-101">Remove-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="19525-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19525-102">SYNOPSIS</span></span>
<span data-ttu-id="19525-103">Usuwa bramę zarządzania serwera.</span><span class="sxs-lookup"><span data-stu-id="19525-103">Removes a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19525-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19525-104">SYNTAX</span></span>

### <span data-ttu-id="19525-105">ByName</span><span class="sxs-lookup"><span data-stu-id="19525-105">ByName</span></span>
```
Remove-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19525-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="19525-106">ByObject</span></span>
```
Remove-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19525-107">Opis</span><span class="sxs-lookup"><span data-stu-id="19525-107">DESCRIPTION</span></span>
<span data-ttu-id="19525-108">Polecenie cmdlet **Remove-AzureRmServerManagementGateway** usuwa bramę zarządzania serwera Azure.</span><span class="sxs-lookup"><span data-stu-id="19525-108">The **Remove-AzureRmServerManagementGateway** cmdlet removes an Azure Server Management gateway.</span></span>

## <span data-ttu-id="19525-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19525-109">EXAMPLES</span></span>

## <span data-ttu-id="19525-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19525-110">PARAMETERS</span></span>

### <span data-ttu-id="19525-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="19525-111">-Gateway</span></span>
<span data-ttu-id="19525-112">Określa bramę, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19525-112">Specifies the gateway that this cmdlet removes.</span></span>

<span data-ttu-id="19525-113">Ten parametr może być stosowany zamiast parametrów *ResourceGroupName* i *bramaname* .</span><span class="sxs-lookup"><span data-stu-id="19525-113">This parameter may be used instead of the *ResourceGroupName* and the *GatewayName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19525-114">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="19525-114">-GatewayName</span></span>
<span data-ttu-id="19525-115">Określa nazwę bramy usuniętej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19525-115">Specifies the name of the gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19525-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19525-116">-ResourceGroupName</span></span>
<span data-ttu-id="19525-117">Określa nazwę grupy zasobów, do której należy brama.</span><span class="sxs-lookup"><span data-stu-id="19525-117">Specifies the name of the resource group in that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19525-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19525-118">-DefaultProfile</span></span>
<span data-ttu-id="19525-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19525-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19525-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19525-120">CommonParameters</span></span>
<span data-ttu-id="19525-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19525-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19525-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19525-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19525-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19525-123">INPUTS</span></span>

### <span data-ttu-id="19525-124">Problem</span><span class="sxs-lookup"><span data-stu-id="19525-124">Gateway</span></span>
<span data-ttu-id="19525-125">Parametr "brama" akceptuje wartość typu "brama" z procesu</span><span class="sxs-lookup"><span data-stu-id="19525-125">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="19525-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19525-126">OUTPUTS</span></span>

## <span data-ttu-id="19525-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19525-127">NOTES</span></span>
* <span data-ttu-id="19525-128">Przed użyciem tego polecenia cmdlet należy usunąć wszystkie węzły w bramie. w przeciwnym razie to polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="19525-128">All the nodes in the Gateway must be removed before using this cmdlet; otherwise this cmdlet will fail.</span></span>

## <span data-ttu-id="19525-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19525-129">RELATED LINKS</span></span>

[<span data-ttu-id="19525-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="19525-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="19525-131">Nowe — AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="19525-131">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)


