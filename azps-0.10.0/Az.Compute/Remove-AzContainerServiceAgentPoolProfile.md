---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 75e019b9c60a45c1bed8e830d9810b1c6a58e732
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893578"
---
# <span data-ttu-id="543eb-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="543eb-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="543eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="543eb-102">SYNOPSIS</span></span>
<span data-ttu-id="543eb-103">Usuwa profil puli agentów z usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="543eb-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="543eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="543eb-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="543eb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="543eb-105">DESCRIPTION</span></span>
<span data-ttu-id="543eb-106">Polecenie cmdlet **Remove-AzContainerServiceAgentPoolProfile** usuwa profil puli agentów z usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="543eb-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="543eb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="543eb-107">EXAMPLES</span></span>

### <span data-ttu-id="543eb-108">Przykład 1: Usuwanie profilu z usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="543eb-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="543eb-109">Pierwsze polecenie uzyskuje usługę kontenera o nazwie CSResourceGroup17 przy użyciu polecenia cmdlet Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="543eb-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="543eb-110">Polecenie zapisuje usługę w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="543eb-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="543eb-111">Drugie polecenie usuwa profil o nazwie AgentPool01 z usługi kontenera w $Container.</span><span class="sxs-lookup"><span data-stu-id="543eb-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="543eb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="543eb-112">PARAMETERS</span></span>

### <span data-ttu-id="543eb-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="543eb-113">-ContainerService</span></span>
<span data-ttu-id="543eb-114">Określa obiekt usługi kontenera, z którego to polecenie cmdlet usuwa profil puli agentów.</span><span class="sxs-lookup"><span data-stu-id="543eb-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="543eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="543eb-115">-DefaultProfile</span></span>
<span data-ttu-id="543eb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="543eb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="543eb-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="543eb-117">-Name</span></span>
<span data-ttu-id="543eb-118">Określa nazwę profilu puli agentów, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="543eb-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="543eb-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="543eb-119">-Confirm</span></span>
<span data-ttu-id="543eb-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="543eb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="543eb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="543eb-121">-WhatIf</span></span>
<span data-ttu-id="543eb-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="543eb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="543eb-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="543eb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="543eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="543eb-124">CommonParameters</span></span>
<span data-ttu-id="543eb-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="543eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="543eb-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="543eb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="543eb-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="543eb-127">INPUTS</span></span>

### <span data-ttu-id="543eb-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="543eb-128">ContainerService</span></span>
<span data-ttu-id="543eb-129">Parametr "ContainerService" akceptuje wartość typu "ContainerService" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="543eb-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="543eb-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="543eb-130">OUTPUTS</span></span>

### <span data-ttu-id="543eb-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="543eb-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="543eb-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="543eb-132">NOTES</span></span>

## <span data-ttu-id="543eb-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="543eb-133">RELATED LINKS</span></span>

[<span data-ttu-id="543eb-134">Dodaj-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="543eb-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="543eb-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="543eb-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


