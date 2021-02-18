---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 2b102274b35d5f4f477376d3da8ad51bc6f0e694
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181482"
---
# <span data-ttu-id="97c62-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="97c62-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="97c62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c62-102">SYNOPSIS</span></span>
<span data-ttu-id="97c62-103">Pobiera poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="97c62-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="97c62-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97c62-104">SYNTAX</span></span>

### <span data-ttu-id="97c62-105">NameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="97c62-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97c62-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97c62-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97c62-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97c62-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97c62-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="97c62-108">DESCRIPTION</span></span>
<span data-ttu-id="97c62-109">Polecenie Get-AzContainerRegistryCredential cmdlet pobiera poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="97c62-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="97c62-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97c62-110">EXAMPLES</span></span>

### <span data-ttu-id="97c62-111">Przykład 1. Uzyskiwanie poświadczeń logowania do rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="97c62-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="97c62-112">To polecenie pobiera poświadczenia logowania dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="97c62-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="97c62-113">Aby uzyskać poświadczenia logowania, dla użytkownika administratora musi być włączony kontener rejestru \` MyRegistry. \`</span><span class="sxs-lookup"><span data-stu-id="97c62-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="97c62-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97c62-114">PARAMETERS</span></span>

### <span data-ttu-id="97c62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c62-115">-DefaultProfile</span></span>
<span data-ttu-id="97c62-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="97c62-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97c62-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="97c62-117">-Name</span></span>
<span data-ttu-id="97c62-118">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="97c62-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="97c62-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="97c62-119">-Registry</span></span>
<span data-ttu-id="97c62-120">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="97c62-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="97c62-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97c62-121">-ResourceGroupName</span></span>
<span data-ttu-id="97c62-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="97c62-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="97c62-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97c62-123">-ResourceId</span></span>
<span data-ttu-id="97c62-124">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="97c62-124">The container registry resource id</span></span>

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

### <span data-ttu-id="97c62-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c62-125">CommonParameters</span></span>
<span data-ttu-id="97c62-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c62-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c62-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97c62-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c62-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97c62-128">INPUTS</span></span>

### <span data-ttu-id="97c62-129">System.String</span><span class="sxs-lookup"><span data-stu-id="97c62-129">System.String</span></span>

## <span data-ttu-id="97c62-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97c62-130">OUTPUTS</span></span>

### <span data-ttu-id="97c62-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="97c62-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="97c62-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97c62-132">NOTES</span></span>

## <span data-ttu-id="97c62-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97c62-133">RELATED LINKS</span></span>

[<span data-ttu-id="97c62-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97c62-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="97c62-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="97c62-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="97c62-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="97c62-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

