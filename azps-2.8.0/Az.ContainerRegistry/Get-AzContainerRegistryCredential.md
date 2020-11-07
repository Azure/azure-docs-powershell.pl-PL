---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 89b3f47953c4074088c1ae5e2cf8e5f51ff383e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706100"
---
# <span data-ttu-id="45fea-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="45fea-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="45fea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45fea-102">SYNOPSIS</span></span>
<span data-ttu-id="45fea-103">Pobiera poświadczenia logowania do rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="45fea-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="45fea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45fea-104">SYNTAX</span></span>

### <span data-ttu-id="45fea-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="45fea-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45fea-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45fea-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45fea-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45fea-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45fea-108">Opis</span><span class="sxs-lookup"><span data-stu-id="45fea-108">DESCRIPTION</span></span>
<span data-ttu-id="45fea-109">Polecenie cmdlet Get-AzContainerRegistryCredential Pobiera poświadczenia logowania do rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="45fea-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="45fea-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45fea-110">EXAMPLES</span></span>

### <span data-ttu-id="45fea-111">Przykład 1: uzyskiwanie poświadczeń logowania do rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="45fea-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="45fea-112">To polecenie pobiera poświadczenia logowania dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="45fea-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="45fea-113">Użytkownik administracyjny musi być włączony do rejestru kontenera, \` \` Aby uzyskać poświadczenia logowania.</span><span class="sxs-lookup"><span data-stu-id="45fea-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="45fea-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45fea-114">PARAMETERS</span></span>

### <span data-ttu-id="45fea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45fea-115">-DefaultProfile</span></span>
<span data-ttu-id="45fea-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="45fea-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45fea-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45fea-117">-Name</span></span>
<span data-ttu-id="45fea-118">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="45fea-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="45fea-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="45fea-119">-Registry</span></span>
<span data-ttu-id="45fea-120">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="45fea-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="45fea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45fea-121">-ResourceGroupName</span></span>
<span data-ttu-id="45fea-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="45fea-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="45fea-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45fea-123">-ResourceId</span></span>
<span data-ttu-id="45fea-124">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="45fea-124">The container registry resource id</span></span>

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

### <span data-ttu-id="45fea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45fea-125">CommonParameters</span></span>
<span data-ttu-id="45fea-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45fea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45fea-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45fea-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45fea-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45fea-128">INPUTS</span></span>

### <span data-ttu-id="45fea-129">System. String</span><span class="sxs-lookup"><span data-stu-id="45fea-129">System.String</span></span>

## <span data-ttu-id="45fea-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45fea-130">OUTPUTS</span></span>

### <span data-ttu-id="45fea-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="45fea-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="45fea-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45fea-132">NOTES</span></span>

## <span data-ttu-id="45fea-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45fea-133">RELATED LINKS</span></span>

[<span data-ttu-id="45fea-134">Nowe — AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="45fea-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="45fea-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="45fea-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="45fea-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="45fea-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)
