---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 19de4ad776814efa55cdff19b2a77673d8581992
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543447"
---
# <span data-ttu-id="0ff5a-101">Remove-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0ff5a-101">Remove-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="0ff5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ff5a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff5a-103">Usuwa zasady dostępu do sieci w trybie JIT.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-103">Deletes a JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ff5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ff5a-104">SYNTAX</span></span>

### <span data-ttu-id="0ff5a-105">ResourceGroupLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0ff5a-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff5a-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="0ff5a-106">ResourceId</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ff5a-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="0ff5a-107">InputObject</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -InputObject <PSRemoveJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ff5a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0ff5a-108">DESCRIPTION</span></span>
<span data-ttu-id="0ff5a-109">Usuwa zasady dostępu do sieci w czasie.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="0ff5a-110">Po wykonaniu tej akcji użytkownik nie będzie mógł żądać tymczasowych połączeń sieciowych na maszynach wirtualnych, które zostały skonfigurowane w usuniętej zasadzie.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="0ff5a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ff5a-111">EXAMPLES</span></span>

### <span data-ttu-id="0ff5a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ff5a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="0ff5a-113">Usuwa zasady dostępu do sieci w czasie.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="0ff5a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ff5a-114">PARAMETERS</span></span>

### <span data-ttu-id="0ff5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff5a-115">-DefaultProfile</span></span>
<span data-ttu-id="0ff5a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ff5a-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0ff5a-117">-InputObject</span></span>
<span data-ttu-id="0ff5a-118">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-118">Input Object.</span></span>

```yaml
Type: PSRemoveJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff5a-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0ff5a-119">-Location</span></span>
<span data-ttu-id="0ff5a-120">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff5a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ff5a-121">-Name</span></span>
<span data-ttu-id="0ff5a-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff5a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ff5a-123">-PassThru</span></span>
<span data-ttu-id="0ff5a-124">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-124">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff5a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ff5a-125">-ResourceGroupName</span></span>
<span data-ttu-id="0ff5a-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ff5a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ff5a-127">-ResourceId</span></span>
<span data-ttu-id="0ff5a-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ff5a-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ff5a-129">-Confirm</span></span>
<span data-ttu-id="0ff5a-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff5a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff5a-131">-WhatIf</span></span>
<span data-ttu-id="0ff5a-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ff5a-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff5a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff5a-134">CommonParameters</span></span>
<span data-ttu-id="0ff5a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff5a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff5a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ff5a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff5a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ff5a-137">INPUTS</span></span>

### <span data-ttu-id="0ff5a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0ff5a-138">System.String</span></span>
<span data-ttu-id="0ff5a-139">Microsoft. Azure. polecenia. Security. cmdlets. JitNetworkAccessPolicies. PSRemoveJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0ff5a-139">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSRemoveJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="0ff5a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ff5a-140">OUTPUTS</span></span>

### <span data-ttu-id="0ff5a-141">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0ff5a-141">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="0ff5a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ff5a-142">NOTES</span></span>

## <span data-ttu-id="0ff5a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ff5a-143">RELATED LINKS</span></span>
