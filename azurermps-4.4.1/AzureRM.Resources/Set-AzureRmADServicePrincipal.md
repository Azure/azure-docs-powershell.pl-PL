---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 67af78e767b8da7764053e3652e25aef53f2877e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549855"
---
# <span data-ttu-id="1afa5-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1afa5-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="1afa5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1afa5-102">SYNOPSIS</span></span>
<span data-ttu-id="1afa5-103">Aktualizuje istniejącego podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1afa5-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1afa5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1afa5-104">SYNTAX</span></span>

### <span data-ttu-id="1afa5-105">SpObjectIdWithDisplayNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1afa5-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afa5-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1afa5-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1afa5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1afa5-107">DESCRIPTION</span></span>
<span data-ttu-id="1afa5-108">Aktualizuje istniejącego podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1afa5-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="1afa5-109">Aby zaktualizować poświadczenia skojarzone z tym podmiotem usługi, użyj New-AzureRmADSpCredential polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1afa5-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="1afa5-110">Aby zaktualizować właściwości skojarzone z aplikacją podstawową, użyj polecenia cmdlet Set-AzureRmADApplication.</span><span class="sxs-lookup"><span data-stu-id="1afa5-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="1afa5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1afa5-111">EXAMPLES</span></span>

### <span data-ttu-id="1afa5-112">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1afa5-112">--------------------------  Example 1  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="1afa5-113">Aktualizuje nazwę wyświetlaną dla podmiotu zabezpieczeń usługi o określonym identyfikatorze obiektu.</span><span class="sxs-lookup"><span data-stu-id="1afa5-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="1afa5-114">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1afa5-114">--------------------------  Example 2  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="1afa5-115">Aktualizuje nazwę wyświetlaną podmiotu usługi o określonej nazwie głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="1afa5-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="1afa5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1afa5-116">PARAMETERS</span></span>

### <span data-ttu-id="1afa5-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1afa5-117">-DisplayName</span></span>
<span data-ttu-id="1afa5-118">Nowa nazwa wyświetlana dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="1afa5-118">New display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1afa5-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1afa5-119">-ObjectId</span></span>
<span data-ttu-id="1afa5-120">Identyfikator obiektu podmiotu usługi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="1afa5-120">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1afa5-121">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1afa5-121">-ServicePrincipalName</span></span>
<span data-ttu-id="1afa5-122">Nazwa SPN głównej usługi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="1afa5-122">The SPN of service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1afa5-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1afa5-123">-Confirm</span></span>
<span data-ttu-id="1afa5-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1afa5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1afa5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1afa5-125">-WhatIf</span></span>
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

### <span data-ttu-id="1afa5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afa5-126">-DefaultProfile</span></span>
<span data-ttu-id="1afa5-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1afa5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1afa5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afa5-128">CommonParameters</span></span>
<span data-ttu-id="1afa5-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1afa5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afa5-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1afa5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afa5-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1afa5-131">INPUTS</span></span>

## <span data-ttu-id="1afa5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1afa5-132">OUTPUTS</span></span>

## <span data-ttu-id="1afa5-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1afa5-133">NOTES</span></span>

## <span data-ttu-id="1afa5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1afa5-134">RELATED LINKS</span></span>

[<span data-ttu-id="1afa5-135">Nowe — AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1afa5-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1afa5-136">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1afa5-136">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1afa5-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1afa5-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1afa5-138">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1afa5-138">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="1afa5-139">Nowe — AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1afa5-139">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="1afa5-140">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1afa5-140">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

