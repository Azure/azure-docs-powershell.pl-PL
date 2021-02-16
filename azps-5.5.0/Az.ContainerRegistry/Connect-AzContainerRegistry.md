---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 3c702d0572bb8e5bdf41deff599b9da6c5cc2dcf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243963"
---
# <span data-ttu-id="fab2c-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fab2c-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="fab2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fab2c-102">SYNOPSIS</span></span>
<span data-ttu-id="fab2c-103">Zaloguj się do rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="fab2c-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="fab2c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fab2c-104">SYNTAX</span></span>

### <span data-ttu-id="fab2c-105">WithoutNameAndPasswordParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="fab2c-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fab2c-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="fab2c-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fab2c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fab2c-107">DESCRIPTION</span></span>
<span data-ttu-id="fab2c-108">Zaloguj się do rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="fab2c-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="fab2c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fab2c-109">EXAMPLES</span></span>

### <span data-ttu-id="fab2c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fab2c-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="fab2c-111">Zaloguj się do usługi ACR bez poświadczeń, gdy już loguj się do konta azure.</span><span class="sxs-lookup"><span data-stu-id="fab2c-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="fab2c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fab2c-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="fab2c-113">Zaloguj się do funkcji ACR przy użyciu nazwy użytkownika/hasła administratora, gdy administrator był włączony.</span><span class="sxs-lookup"><span data-stu-id="fab2c-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="fab2c-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="fab2c-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="fab2c-115">Zaloguj się do usługi ACR przy użyciu identyfikatora aplikacji podmiotu zabezpieczeń usługi i hasła.</span><span class="sxs-lookup"><span data-stu-id="fab2c-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="fab2c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fab2c-116">PARAMETERS</span></span>

### <span data-ttu-id="fab2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab2c-117">-DefaultProfile</span></span>
<span data-ttu-id="fab2c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fab2c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fab2c-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fab2c-119">-Name</span></span>
<span data-ttu-id="fab2c-120">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fab2c-120">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab2c-121">— Hasło</span><span class="sxs-lookup"><span data-stu-id="fab2c-121">-Password</span></span>
<span data-ttu-id="fab2c-122">Hasło dla rejestru Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="fab2c-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fab2c-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="fab2c-123">-UserName</span></span>
<span data-ttu-id="fab2c-124">Nazwa użytkownika rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="fab2c-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fab2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab2c-125">CommonParameters</span></span>
<span data-ttu-id="fab2c-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab2c-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fab2c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab2c-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fab2c-128">INPUTS</span></span>

### <span data-ttu-id="fab2c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fab2c-129">System.String</span></span>

## <span data-ttu-id="fab2c-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fab2c-130">OUTPUTS</span></span>

### <span data-ttu-id="fab2c-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fab2c-131">System.Boolean</span></span>

## <span data-ttu-id="fab2c-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fab2c-132">NOTES</span></span>

## <span data-ttu-id="fab2c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fab2c-133">RELATED LINKS</span></span>
