---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 46eb802b4a91aa7ee7d370ed9ca93805497f21d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546835"
---
# <span data-ttu-id="c9bbf-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c9bbf-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="c9bbf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="c9bbf-103">Generuje ponownie poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9bbf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9bbf-104">SYNTAX</span></span>

### <span data-ttu-id="c9bbf-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c9bbf-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9bbf-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9bbf-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9bbf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9bbf-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9bbf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c9bbf-108">DESCRIPTION</span></span>
<span data-ttu-id="c9bbf-109">Polecenie cmdlet Update-AzureRmContainerRegistryCredential ponownie generuje poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="c9bbf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9bbf-110">EXAMPLES</span></span>

### <span data-ttu-id="c9bbf-111">Przykład 1. Regeneruj ponownie poświadczenia logowania dla rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="c9bbf-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="c9bbf-112">To polecenie generuje ponownie poświadczenia logowania dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="c9bbf-113">Administrator musi być włączony w rejestrze kontenera rejestru, \` \` Aby ponownie wygenerować poświadczenia logowania.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="c9bbf-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9bbf-114">PARAMETERS</span></span>

### <span data-ttu-id="c9bbf-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9bbf-115">-Name</span></span>
<span data-ttu-id="c9bbf-116">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-116">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bbf-117">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="c9bbf-117">-PasswordName</span></span>
<span data-ttu-id="c9bbf-118">Nazwa hasła do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-118">The name of password to regenerate.</span></span>
<span data-ttu-id="c9bbf-119">Dozwolone wartości: Password (hasło), password2.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-119">Allowed values: password, password2.</span></span>

```yaml
Type: PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bbf-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="c9bbf-120">-Registry</span></span>
<span data-ttu-id="c9bbf-121">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-121">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9bbf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9bbf-122">-ResourceGroupName</span></span>
<span data-ttu-id="c9bbf-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bbf-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9bbf-124">-Confirm</span></span>
<span data-ttu-id="c9bbf-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bbf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9bbf-126">-WhatIf</span></span>
<span data-ttu-id="c9bbf-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9bbf-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bbf-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9bbf-129">-DefaultProfile</span></span>
<span data-ttu-id="c9bbf-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c9bbf-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9bbf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9bbf-131">-ResourceId</span></span>
<span data-ttu-id="c9bbf-132">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="c9bbf-132">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9bbf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9bbf-133">CommonParameters</span></span>
<span data-ttu-id="c9bbf-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9bbf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9bbf-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9bbf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9bbf-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9bbf-136">INPUTS</span></span>

### <span data-ttu-id="c9bbf-137">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c9bbf-137">PSContainerRegistry</span></span>
<span data-ttu-id="c9bbf-138">Parametr "Registry" przyjmuje wartość typu "PSContainerRegistry" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c9bbf-138">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="c9bbf-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9bbf-139">OUTPUTS</span></span>

### <span data-ttu-id="c9bbf-140">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c9bbf-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="c9bbf-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9bbf-141">NOTES</span></span>

## <span data-ttu-id="c9bbf-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9bbf-142">RELATED LINKS</span></span>

[<span data-ttu-id="c9bbf-143">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c9bbf-143">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="c9bbf-144">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c9bbf-144">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="c9bbf-145">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c9bbf-145">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

