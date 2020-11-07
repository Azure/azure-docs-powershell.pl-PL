---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: cfcb3c7657bc0ff99646c3ef21eb5cceb592fe2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716635"
---
# <span data-ttu-id="78386-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="78386-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="78386-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78386-102">SYNOPSIS</span></span>
<span data-ttu-id="78386-103">Usuwa profil puli agentów z usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="78386-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78386-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78386-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [-Name] <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78386-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78386-105">DESCRIPTION</span></span>
<span data-ttu-id="78386-106">Polecenie cmdlet **Remove-AzureRmContainerServiceAgentPoolProfile** usuwa profil puli agentów z usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="78386-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="78386-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78386-107">EXAMPLES</span></span>

### <span data-ttu-id="78386-108">Przykład 1: Usuwanie profilu z usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="78386-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="78386-109">Pierwsze polecenie uzyskuje usługę kontenera o nazwie CSResourceGroup17 przy użyciu polecenia cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="78386-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="78386-110">Polecenie zapisuje usługę w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="78386-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="78386-111">Drugie polecenie usuwa profil o nazwie AgentPool01 z usługi kontenera w $Container.</span><span class="sxs-lookup"><span data-stu-id="78386-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="78386-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78386-112">PARAMETERS</span></span>

### <span data-ttu-id="78386-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="78386-113">-ContainerService</span></span>
<span data-ttu-id="78386-114">Określa obiekt usługi kontenera, z którego to polecenie cmdlet usuwa profil puli agentów.</span><span class="sxs-lookup"><span data-stu-id="78386-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78386-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78386-115">-Name</span></span>
<span data-ttu-id="78386-116">Określa nazwę profilu puli agentów, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78386-116">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78386-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78386-117">-Confirm</span></span>
<span data-ttu-id="78386-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78386-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78386-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78386-119">-WhatIf</span></span>
<span data-ttu-id="78386-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78386-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78386-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="78386-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78386-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78386-122">CommonParameters</span></span>
<span data-ttu-id="78386-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78386-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78386-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78386-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78386-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78386-125">INPUTS</span></span>

### <span data-ttu-id="78386-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="78386-126">None</span></span>
<span data-ttu-id="78386-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="78386-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78386-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78386-128">OUTPUTS</span></span>

## <span data-ttu-id="78386-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78386-129">NOTES</span></span>

## <span data-ttu-id="78386-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78386-130">RELATED LINKS</span></span>

[<span data-ttu-id="78386-131">Dodaj-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="78386-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="78386-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="78386-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


