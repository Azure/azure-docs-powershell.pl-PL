---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: fc9d8db7f293ff94e33b50afd55176d157046fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548319"
---
# <span data-ttu-id="a948d-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a948d-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="a948d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a948d-102">SYNOPSIS</span></span>
<span data-ttu-id="a948d-103">Pobiera poświadczenia logowania do rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="a948d-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a948d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a948d-104">SYNTAX</span></span>

### <span data-ttu-id="a948d-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a948d-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a948d-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a948d-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a948d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a948d-107">DESCRIPTION</span></span>
<span data-ttu-id="a948d-108">Polecenie cmdlet **Get-AzureRmContainerRegistryCredential** Pobiera poświadczenia logowania do rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="a948d-108">The **Get-AzureRmContainerRegistryCredential** cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="a948d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a948d-109">EXAMPLES</span></span>

### <span data-ttu-id="a948d-110">Przykład 1: uzyskiwanie poświadczeń logowania do rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="a948d-110">Example 1: Get the login credentials for a container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="a948d-111">To polecenie pobiera poświadczenia logowania dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="a948d-111">This command gets the login credentials for the specified container registry.</span></span> <span data-ttu-id="a948d-112">Użytkownik administracyjny musi być włączony dla rejestru kontenera, `MyRegistry` Aby uzyskać poświadczenia logowania.</span><span class="sxs-lookup"><span data-stu-id="a948d-112">Admin user has to be enabled for the container registry `MyRegistry` to get login credentials.</span></span>

## <span data-ttu-id="a948d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a948d-113">PARAMETERS</span></span>

### <span data-ttu-id="a948d-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a948d-114">-Name</span></span>
<span data-ttu-id="a948d-115">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="a948d-115">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a948d-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="a948d-116">-Registry</span></span>
<span data-ttu-id="a948d-117">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="a948d-117">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a948d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a948d-118">-ResourceGroupName</span></span>
<span data-ttu-id="a948d-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a948d-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a948d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a948d-120">-DefaultProfile</span></span>
<span data-ttu-id="a948d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a948d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a948d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a948d-122">CommonParameters</span></span>
<span data-ttu-id="a948d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a948d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a948d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a948d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a948d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a948d-125">INPUTS</span></span>

### <span data-ttu-id="a948d-126">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a948d-126">PSContainerRegistry</span></span>
<span data-ttu-id="a948d-127">Parametr "Registry" przyjmuje wartość typu "PSContainerRegistry" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="a948d-127">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="a948d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a948d-128">OUTPUTS</span></span>

### <span data-ttu-id="a948d-129">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a948d-129">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="a948d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a948d-130">NOTES</span></span>

## <span data-ttu-id="a948d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a948d-131">RELATED LINKS</span></span>

[<span data-ttu-id="a948d-132">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a948d-132">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="a948d-133">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a948d-133">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="a948d-134">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a948d-134">Update-AzureRmContainerRegistryCredential</span></span>](./Update-AzureRmContainerRegistryCredential.md)

