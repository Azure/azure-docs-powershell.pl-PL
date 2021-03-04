---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: be045303db770cbba919d27ed9563aa64283572c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004458"
---
# <span data-ttu-id="c430d-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c430d-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="c430d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c430d-102">SYNOPSIS</span></span>
<span data-ttu-id="c430d-103">Zaloguj się do rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="c430d-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="c430d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c430d-104">SYNTAX</span></span>

### <span data-ttu-id="c430d-105">WithoutNameAndPasswordParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="c430d-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c430d-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="c430d-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c430d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c430d-107">DESCRIPTION</span></span>
<span data-ttu-id="c430d-108">Zaloguj się do rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="c430d-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="c430d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c430d-109">EXAMPLES</span></span>

### <span data-ttu-id="c430d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c430d-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="c430d-111">Zaloguj się do usługi ACR bez poświadczeń, gdy już loguj się do konta azure.</span><span class="sxs-lookup"><span data-stu-id="c430d-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="c430d-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c430d-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="c430d-113">Zaloguj się do funkcji ACR przy użyciu nazwy użytkownika/hasła administratora, gdy administrator był włączony.</span><span class="sxs-lookup"><span data-stu-id="c430d-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="c430d-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c430d-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="c430d-115">Zaloguj się do usługi ACR przy użyciu identyfikatora aplikacji podmiotu zabezpieczeń usługi i hasła.</span><span class="sxs-lookup"><span data-stu-id="c430d-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="c430d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c430d-116">PARAMETERS</span></span>

### <span data-ttu-id="c430d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c430d-117">-DefaultProfile</span></span>
<span data-ttu-id="c430d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c430d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c430d-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c430d-119">-Name</span></span>
<span data-ttu-id="c430d-120">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c430d-120">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="c430d-121">— Hasło</span><span class="sxs-lookup"><span data-stu-id="c430d-121">-Password</span></span>
<span data-ttu-id="c430d-122">Hasło dla rejestru Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="c430d-122">Password For Azure Container Registry.</span></span>

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

### <span data-ttu-id="c430d-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="c430d-123">-UserName</span></span>
<span data-ttu-id="c430d-124">Nazwa użytkownika rejestru azure container.</span><span class="sxs-lookup"><span data-stu-id="c430d-124">User Name For Azure Container Registry.</span></span>

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

### <span data-ttu-id="c430d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c430d-125">CommonParameters</span></span>
<span data-ttu-id="c430d-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c430d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c430d-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c430d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c430d-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c430d-128">INPUTS</span></span>

### <span data-ttu-id="c430d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c430d-129">System.String</span></span>

## <span data-ttu-id="c430d-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c430d-130">OUTPUTS</span></span>

### <span data-ttu-id="c430d-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c430d-131">System.Boolean</span></span>

## <span data-ttu-id="c430d-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c430d-132">NOTES</span></span>

## <span data-ttu-id="c430d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c430d-133">RELATED LINKS</span></span>
