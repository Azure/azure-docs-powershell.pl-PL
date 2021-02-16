---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200106"
---
# <span data-ttu-id="6f04a-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="6f04a-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="6f04a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f04a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f04a-103">Wygeneruj klucz aplikacji Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="6f04a-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="6f04a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6f04a-104">SYNTAX</span></span>

### <span data-ttu-id="6f04a-105">ResourceSet (Default)</span><span class="sxs-lookup"><span data-stu-id="6f04a-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f04a-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6f04a-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f04a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6f04a-107">DESCRIPTION</span></span>
<span data-ttu-id="6f04a-108">Wygeneruj klucz aplikacji Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="6f04a-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="6f04a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6f04a-109">EXAMPLES</span></span>

### <span data-ttu-id="6f04a-110">Przykład 1. Ponowne generowanie klucza podstawowego</span><span class="sxs-lookup"><span data-stu-id="6f04a-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="6f04a-111">Ponownie wygenerowany klucz podstawowy dla zasad autoryzacji "klucz testowy" centrum azure iot.</span><span class="sxs-lookup"><span data-stu-id="6f04a-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="6f04a-112">Przykład 2. Zamiana klawiszy</span><span class="sxs-lookup"><span data-stu-id="6f04a-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="6f04a-113">Klucze zamiany dla zasad autoryzacji "klucz testowy" centrum azure iot.</span><span class="sxs-lookup"><span data-stu-id="6f04a-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="6f04a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f04a-114">PARAMETERS</span></span>

### <span data-ttu-id="6f04a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f04a-115">-DefaultProfile</span></span>
<span data-ttu-id="6f04a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6f04a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f04a-117">— HubId</span><span class="sxs-lookup"><span data-stu-id="6f04a-117">-HubId</span></span>
<span data-ttu-id="6f04a-118">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="6f04a-118">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f04a-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6f04a-119">-KeyName</span></span>
<span data-ttu-id="6f04a-120">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="6f04a-120">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f04a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6f04a-121">-Name</span></span>
<span data-ttu-id="6f04a-122">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="6f04a-122">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f04a-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="6f04a-123">-RenewKey</span></span>
<span data-ttu-id="6f04a-124">Ponownie wygeneruj klucz.</span><span class="sxs-lookup"><span data-stu-id="6f04a-124">Regenerate Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f04a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f04a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f04a-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6f04a-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f04a-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6f04a-127">-Confirm</span></span>
<span data-ttu-id="6f04a-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6f04a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f04a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f04a-129">-WhatIf</span></span>
<span data-ttu-id="6f04a-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f04a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f04a-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6f04a-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f04a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f04a-132">CommonParameters</span></span>
<span data-ttu-id="6f04a-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f04a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f04a-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f04a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f04a-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f04a-135">INPUTS</span></span>

### <span data-ttu-id="6f04a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6f04a-136">System.String</span></span>

## <span data-ttu-id="6f04a-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f04a-137">OUTPUTS</span></span>

### <span data-ttu-id="6f04a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6f04a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="6f04a-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6f04a-139">NOTES</span></span>

## <span data-ttu-id="6f04a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f04a-140">RELATED LINKS</span></span>
