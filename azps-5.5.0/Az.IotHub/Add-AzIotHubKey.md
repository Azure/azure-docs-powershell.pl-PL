---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188251"
---
# <span data-ttu-id="650fb-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="650fb-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="650fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="650fb-102">SYNOPSIS</span></span>
<span data-ttu-id="650fb-103">Tworzy klucz aplikacji IotHub.</span><span class="sxs-lookup"><span data-stu-id="650fb-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="650fb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="650fb-104">SYNTAX</span></span>

### <span data-ttu-id="650fb-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="650fb-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="650fb-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="650fb-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="650fb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="650fb-107">DESCRIPTION</span></span>
<span data-ttu-id="650fb-108">Tworzy klucz dla podanej usługi IotHub.</span><span class="sxs-lookup"><span data-stu-id="650fb-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="650fb-109">Nazwy kluczy nie są unikatowe i trzeba nimi ostrożnie zarządzać.</span><span class="sxs-lookup"><span data-stu-id="650fb-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="650fb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="650fb-110">EXAMPLES</span></span>

### <span data-ttu-id="650fb-111">Przykład 1. Dodawanie klucza do aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="650fb-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="650fb-112">Tworzy klucz o nazwie "mykey" dla aplikacji iothub "myiothub" z uprawnieniami RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="650fb-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="650fb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="650fb-113">PARAMETERS</span></span>

### <span data-ttu-id="650fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650fb-114">-DefaultProfile</span></span>
<span data-ttu-id="650fb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="650fb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="650fb-116">— HubId</span><span class="sxs-lookup"><span data-stu-id="650fb-116">-HubId</span></span>
<span data-ttu-id="650fb-117">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="650fb-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="650fb-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="650fb-118">-KeyName</span></span>
<span data-ttu-id="650fb-119">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="650fb-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650fb-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="650fb-120">-Name</span></span>
<span data-ttu-id="650fb-121">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="650fb-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="650fb-122">- Klucz Podstawowy</span><span class="sxs-lookup"><span data-stu-id="650fb-122">-PrimaryKey</span></span>
<span data-ttu-id="650fb-123">Klucz podstawowy</span><span class="sxs-lookup"><span data-stu-id="650fb-123">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="650fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="650fb-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="650fb-125">Resource Group Name</span></span>

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

### <span data-ttu-id="650fb-126">— Prawa</span><span class="sxs-lookup"><span data-stu-id="650fb-126">-Rights</span></span>
<span data-ttu-id="650fb-127">Uprawnienia dla tej aplikacji IOTHub</span><span class="sxs-lookup"><span data-stu-id="650fb-127">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650fb-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="650fb-128">-SecondaryKey</span></span>
<span data-ttu-id="650fb-129">Klucz pomocniczy</span><span class="sxs-lookup"><span data-stu-id="650fb-129">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="650fb-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="650fb-130">-Confirm</span></span>
<span data-ttu-id="650fb-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="650fb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="650fb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="650fb-132">-WhatIf</span></span>
<span data-ttu-id="650fb-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="650fb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="650fb-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="650fb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="650fb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650fb-135">CommonParameters</span></span>
<span data-ttu-id="650fb-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="650fb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="650fb-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="650fb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650fb-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="650fb-138">INPUTS</span></span>

### <span data-ttu-id="650fb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="650fb-139">System.String</span></span>

## <span data-ttu-id="650fb-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="650fb-140">OUTPUTS</span></span>

### <span data-ttu-id="650fb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="650fb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="650fb-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="650fb-142">NOTES</span></span>

## <span data-ttu-id="650fb-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="650fb-143">RELATED LINKS</span></span>
