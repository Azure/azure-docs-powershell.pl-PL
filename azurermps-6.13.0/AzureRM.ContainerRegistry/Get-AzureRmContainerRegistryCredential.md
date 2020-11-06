---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 37ca6fad019814c476f48d1f086a430db75afb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524514"
---
# <span data-ttu-id="01576-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="01576-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="01576-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01576-102">SYNOPSIS</span></span>
<span data-ttu-id="01576-103">Pobiera poświadczenia logowania do rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="01576-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01576-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01576-104">SYNTAX</span></span>

### <span data-ttu-id="01576-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="01576-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01576-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01576-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01576-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01576-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01576-108">Opis</span><span class="sxs-lookup"><span data-stu-id="01576-108">DESCRIPTION</span></span>
<span data-ttu-id="01576-109">Polecenie cmdlet Get-AzureRmContainerRegistryCredential Pobiera poświadczenia logowania do rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="01576-109">The Get-AzureRmContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="01576-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01576-110">EXAMPLES</span></span>

### <span data-ttu-id="01576-111">Przykład 1: uzyskiwanie poświadczeń logowania do rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="01576-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="01576-112">To polecenie pobiera poświadczenia logowania dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="01576-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="01576-113">Użytkownik administracyjny musi być włączony do rejestru kontenera, \` \` Aby uzyskać poświadczenia logowania.</span><span class="sxs-lookup"><span data-stu-id="01576-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="01576-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01576-114">PARAMETERS</span></span>

### <span data-ttu-id="01576-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01576-115">-DefaultProfile</span></span>
<span data-ttu-id="01576-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="01576-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01576-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01576-117">-Name</span></span>
<span data-ttu-id="01576-118">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="01576-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="01576-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="01576-119">-Registry</span></span>
<span data-ttu-id="01576-120">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="01576-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01576-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01576-121">-ResourceGroupName</span></span>
<span data-ttu-id="01576-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="01576-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="01576-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01576-123">-ResourceId</span></span>
<span data-ttu-id="01576-124">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="01576-124">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01576-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01576-125">CommonParameters</span></span>
<span data-ttu-id="01576-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01576-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01576-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01576-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01576-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01576-128">INPUTS</span></span>

### <span data-ttu-id="01576-129">System. String</span><span class="sxs-lookup"><span data-stu-id="01576-129">System.String</span></span>

## <span data-ttu-id="01576-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01576-130">OUTPUTS</span></span>

### <span data-ttu-id="01576-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="01576-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="01576-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01576-132">NOTES</span></span>

## <span data-ttu-id="01576-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01576-133">RELATED LINKS</span></span>

[<span data-ttu-id="01576-134">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="01576-134">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="01576-135">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="01576-135">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="01576-136">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="01576-136">Update-AzureRmContainerRegistryCredential</span></span>](Update-AzureRmContainerRegistryCredential.md)

