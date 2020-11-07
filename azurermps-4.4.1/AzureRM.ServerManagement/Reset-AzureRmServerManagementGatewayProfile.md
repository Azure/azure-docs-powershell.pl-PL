---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 9ce8dc1faf1a762a847da5eb87fb28b510308054
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717788"
---
# <span data-ttu-id="b94ac-101">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="b94ac-101">Reset-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="b94ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b94ac-102">SYNOPSIS</span></span>
<span data-ttu-id="b94ac-103">Resetuje profil bramy zarządzania serwera.</span><span class="sxs-lookup"><span data-stu-id="b94ac-103">Resets the profile of a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b94ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b94ac-104">SYNTAX</span></span>

### <span data-ttu-id="b94ac-105">ByName</span><span class="sxs-lookup"><span data-stu-id="b94ac-105">ByName</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b94ac-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="b94ac-106">ByObject</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b94ac-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b94ac-107">DESCRIPTION</span></span>
<span data-ttu-id="b94ac-108">Polecenie cmdlet **Reset-AzureRmServerManagementGatewayProfile** resetuje profil bramy zarządzania programu Azure Server.</span><span class="sxs-lookup"><span data-stu-id="b94ac-108">The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.</span></span>

<span data-ttu-id="b94ac-109">Aby pobrać profil, należy użyć polecenia cmdlet Save-AzureRmServerManagementGatewayProfile, a następnie Install-AzureRmServerManagementGatewayProfile polecenia cmdlet w celu zapisania go po zresetowaniu profilu.</span><span class="sxs-lookup"><span data-stu-id="b94ac-109">You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.</span></span>

## <span data-ttu-id="b94ac-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b94ac-110">EXAMPLES</span></span>

## <span data-ttu-id="b94ac-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b94ac-111">PARAMETERS</span></span>

### <span data-ttu-id="b94ac-112">-Gateway</span><span class="sxs-lookup"><span data-stu-id="b94ac-112">-Gateway</span></span>
<span data-ttu-id="b94ac-113">Określa bramę, dla której jest resetowany profil.</span><span class="sxs-lookup"><span data-stu-id="b94ac-113">Specifies the gateway for which the cmdlet resets the profile for.</span></span>

<span data-ttu-id="b94ac-114">Można określić zamiast ResourceGoupName i Gatewayname</span><span class="sxs-lookup"><span data-stu-id="b94ac-114">May be specified instead of ResourceGoupName and GatewayName</span></span>

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

### <span data-ttu-id="b94ac-115">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="b94ac-115">-GatewayName</span></span>
<span data-ttu-id="b94ac-116">Określa nazwę bramy, dla której polecenie cmdlet resetuje profil.</span><span class="sxs-lookup"><span data-stu-id="b94ac-116">Specifies the name of the gateway for which the cmdlet resets the profile.</span></span>

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

### <span data-ttu-id="b94ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b94ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="b94ac-118">Określa nazwę grupy zasobów, do której należy brama.</span><span class="sxs-lookup"><span data-stu-id="b94ac-118">Specifies the name of the resource group that the gateway belongs to.</span></span>

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

### <span data-ttu-id="b94ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b94ac-119">-DefaultProfile</span></span>
<span data-ttu-id="b94ac-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b94ac-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b94ac-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b94ac-121">CommonParameters</span></span>
<span data-ttu-id="b94ac-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b94ac-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b94ac-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b94ac-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b94ac-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b94ac-124">INPUTS</span></span>

### <span data-ttu-id="b94ac-125">Problem</span><span class="sxs-lookup"><span data-stu-id="b94ac-125">Gateway</span></span>
<span data-ttu-id="b94ac-126">Parametr "brama" akceptuje wartość typu "brama" z procesu</span><span class="sxs-lookup"><span data-stu-id="b94ac-126">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="b94ac-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b94ac-127">OUTPUTS</span></span>

## <span data-ttu-id="b94ac-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b94ac-128">NOTES</span></span>

## <span data-ttu-id="b94ac-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b94ac-129">RELATED LINKS</span></span>

[<span data-ttu-id="b94ac-130">Zainstaluj — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="b94ac-130">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="b94ac-131">Zapisz — AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="b94ac-131">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


