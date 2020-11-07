---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 3b9b31530d467f0c31ea3ade4968118042fee47b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868816"
---
# <span data-ttu-id="c7b1c-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c7b1c-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="c7b1c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b1c-103">Pobiera poświadczenia logowania do rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="c7b1c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7b1c-104">SYNTAX</span></span>

### <span data-ttu-id="c7b1c-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c7b1c-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7b1c-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7b1c-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7b1c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7b1c-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7b1c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c7b1c-108">DESCRIPTION</span></span>
<span data-ttu-id="c7b1c-109">Polecenie cmdlet Get-AzContainerRegistryCredential Pobiera poświadczenia logowania do rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="c7b1c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7b1c-110">EXAMPLES</span></span>

### <span data-ttu-id="c7b1c-111">Przykład 1: uzyskiwanie poświadczeń logowania do rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="c7b1c-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="c7b1c-112">To polecenie pobiera poświadczenia logowania dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="c7b1c-113">Użytkownik administracyjny musi być włączony do rejestru kontenera, \` \` Aby uzyskać poświadczenia logowania.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="c7b1c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7b1c-114">PARAMETERS</span></span>

### <span data-ttu-id="c7b1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b1c-115">-DefaultProfile</span></span>
<span data-ttu-id="c7b1c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c7b1c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7b1c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c7b1c-117">-Name</span></span>
<span data-ttu-id="c7b1c-118">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="c7b1c-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="c7b1c-119">-Registry</span></span>
<span data-ttu-id="c7b1c-120">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="c7b1c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7b1c-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7b1c-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7b1c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b1c-123">-ResourceId</span></span>
<span data-ttu-id="c7b1c-124">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="c7b1c-124">The container registry resource id</span></span>

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

### <span data-ttu-id="c7b1c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b1c-125">CommonParameters</span></span>
<span data-ttu-id="c7b1c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b1c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b1c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7b1c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b1c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7b1c-128">INPUTS</span></span>

### <span data-ttu-id="c7b1c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c7b1c-129">System.String</span></span>

## <span data-ttu-id="c7b1c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7b1c-130">OUTPUTS</span></span>

### <span data-ttu-id="c7b1c-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c7b1c-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="c7b1c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7b1c-132">NOTES</span></span>

## <span data-ttu-id="c7b1c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7b1c-133">RELATED LINKS</span></span>

[<span data-ttu-id="c7b1c-134">Nowe — AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c7b1c-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="c7b1c-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c7b1c-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="c7b1c-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c7b1c-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

