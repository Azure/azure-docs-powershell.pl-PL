---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898961"
---
# <span data-ttu-id="2b94a-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="2b94a-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="2b94a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b94a-102">SYNOPSIS</span></span>
<span data-ttu-id="2b94a-103">Usuwa profil puli agentów z usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="2b94a-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b94a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b94a-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b94a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b94a-105">DESCRIPTION</span></span>
<span data-ttu-id="2b94a-106">Polecenie cmdlet **Remove-AzureRmContainerServiceAgentPoolProfile** usuwa profil puli agentów z usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="2b94a-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="2b94a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b94a-107">EXAMPLES</span></span>

### <span data-ttu-id="2b94a-108">Przykład 1: Usuwanie profilu z usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="2b94a-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="2b94a-109">Pierwsze polecenie uzyskuje usługę kontenera o nazwie CSResourceGroup17 przy użyciu polecenia cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="2b94a-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="2b94a-110">Polecenie zapisuje usługę w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="2b94a-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="2b94a-111">Drugie polecenie usuwa profil o nazwie AgentPool01 z usługi kontenera w $Container.</span><span class="sxs-lookup"><span data-stu-id="2b94a-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="2b94a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b94a-112">PARAMETERS</span></span>

### <span data-ttu-id="2b94a-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="2b94a-113">-ContainerService</span></span>
<span data-ttu-id="2b94a-114">Określa obiekt usługi kontenera, z którego to polecenie cmdlet usuwa profil puli agentów.</span><span class="sxs-lookup"><span data-stu-id="2b94a-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

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

### <span data-ttu-id="2b94a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b94a-115">-DefaultProfile</span></span>
<span data-ttu-id="2b94a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b94a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b94a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b94a-117">-Name</span></span>
<span data-ttu-id="2b94a-118">Określa nazwę profilu puli agentów, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b94a-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2b94a-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b94a-119">-Confirm</span></span>
<span data-ttu-id="2b94a-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b94a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b94a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b94a-121">-WhatIf</span></span>
<span data-ttu-id="2b94a-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b94a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b94a-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b94a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b94a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b94a-124">CommonParameters</span></span>
<span data-ttu-id="2b94a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b94a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b94a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b94a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b94a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b94a-127">INPUTS</span></span>

### <span data-ttu-id="2b94a-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="2b94a-128">ContainerService</span></span>
<span data-ttu-id="2b94a-129">Parametr "ContainerService" akceptuje wartość typu "ContainerService" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="2b94a-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="2b94a-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b94a-130">OUTPUTS</span></span>

### <span data-ttu-id="2b94a-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="2b94a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="2b94a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b94a-132">NOTES</span></span>

## <span data-ttu-id="2b94a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b94a-133">RELATED LINKS</span></span>

[<span data-ttu-id="2b94a-134">Dodaj-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="2b94a-134">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="2b94a-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2b94a-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


