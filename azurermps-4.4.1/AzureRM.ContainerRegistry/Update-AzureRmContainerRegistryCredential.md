---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: e65367a94e946aee83df2087463bd0081e925862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717177"
---
# <span data-ttu-id="ebfa0-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ebfa0-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="ebfa0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebfa0-102">SYNOPSIS</span></span>
<span data-ttu-id="ebfa0-103">Generuje ponownie poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebfa0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebfa0-104">SYNTAX</span></span>

### <span data-ttu-id="ebfa0-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ebfa0-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebfa0-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebfa0-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebfa0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ebfa0-107">DESCRIPTION</span></span>
<span data-ttu-id="ebfa0-108">Polecenie cmdlet **Update-AzureRmContainerRegistryCredential** ponownie generuje poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-108">The **Update-AzureRmContainerRegistryCredential** cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="ebfa0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebfa0-109">EXAMPLES</span></span>

### <span data-ttu-id="ebfa0-110">Przykład 1. Regeneruj ponownie poświadczenia logowania dla rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="ebfa0-110">Example 1: Regenerate a login credential for a container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="ebfa0-111">To polecenie generuje ponownie poświadczenia logowania dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-111">This command regenerates a login credential for the specified container registry.</span></span> <span data-ttu-id="ebfa0-112">Aby ponownie wygenerować poświadczenia logowania, użytkownik administracyjny musi być włączony dla rejestru kontenera `MyRegistry` .</span><span class="sxs-lookup"><span data-stu-id="ebfa0-112">Admin user has to be enabled for the container registry `MyRegistry` to regenerate login credentials.</span></span>

## <span data-ttu-id="ebfa0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebfa0-113">PARAMETERS</span></span>

### <span data-ttu-id="ebfa0-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ebfa0-114">-Name</span></span>
<span data-ttu-id="ebfa0-115">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="ebfa0-116">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="ebfa0-116">-PasswordName</span></span>
<span data-ttu-id="ebfa0-117">Nazwa hasła do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-117">The name of password to regenerate.</span></span>
<span data-ttu-id="ebfa0-118">Dozwolone wartości: Password (hasło), password2.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-118">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfa0-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="ebfa0-119">-Registry</span></span>
<span data-ttu-id="ebfa0-120">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="ebfa0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebfa0-121">-ResourceGroupName</span></span>
<span data-ttu-id="ebfa0-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="ebfa0-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ebfa0-123">-Confirm</span></span>
<span data-ttu-id="ebfa0-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfa0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebfa0-125">-WhatIf</span></span>
<span data-ttu-id="ebfa0-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebfa0-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfa0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebfa0-128">-DefaultProfile</span></span>
<span data-ttu-id="ebfa0-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebfa0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebfa0-130">CommonParameters</span></span>
<span data-ttu-id="ebfa0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebfa0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebfa0-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebfa0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebfa0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebfa0-133">INPUTS</span></span>

### <span data-ttu-id="ebfa0-134">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ebfa0-134">PSContainerRegistry</span></span>
<span data-ttu-id="ebfa0-135">Parametr "Registry" przyjmuje wartość typu "PSContainerRegistry" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ebfa0-135">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="ebfa0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebfa0-136">OUTPUTS</span></span>

### <span data-ttu-id="ebfa0-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ebfa0-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="ebfa0-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebfa0-138">NOTES</span></span>

## <span data-ttu-id="ebfa0-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebfa0-139">RELATED LINKS</span></span>

[<span data-ttu-id="ebfa0-140">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ebfa0-140">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="ebfa0-141">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ebfa0-141">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="ebfa0-142">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ebfa0-142">Get-AzureRmContainerRegistryCredential</span></span>](./Get-AzureRmContainerRegistryCredential.md)

