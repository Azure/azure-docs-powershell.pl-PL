---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 89e727b836f28ac1972bcf15e872e2860a8a6672
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176675"
---
# <span data-ttu-id="76378-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="76378-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="76378-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76378-102">SYNOPSIS</span></span>
<span data-ttu-id="76378-103">Ustawia poświadczenia konta magazynu dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="76378-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="76378-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76378-104">SYNTAX</span></span>

### <span data-ttu-id="76378-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="76378-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76378-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76378-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76378-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76378-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76378-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="76378-108">DESCRIPTION</span></span>
<span data-ttu-id="76378-109">Polecenie **cmdlet Set-AzStackEdgeStorageAccountCredential** aktualizuje poświadczenia konta magazynu odpowiadające kontu magazynu na urządzeniu Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="76378-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="76378-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76378-110">EXAMPLES</span></span>

### <span data-ttu-id="76378-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76378-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="76378-112">Pomaga w obracaniu klawiszy dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="76378-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="76378-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76378-113">PARAMETERS</span></span>

### <span data-ttu-id="76378-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="76378-114">-AsJob</span></span>
<span data-ttu-id="76378-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="76378-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76378-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76378-116">-DefaultProfile</span></span>
<span data-ttu-id="76378-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="76378-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76378-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="76378-118">-DeviceName</span></span>
<span data-ttu-id="76378-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="76378-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76378-120">— Klucz szyfrowania</span><span class="sxs-lookup"><span data-stu-id="76378-120">-EncryptionKey</span></span>
<span data-ttu-id="76378-121">Klucz szyfrowania urządzenia Edge</span><span class="sxs-lookup"><span data-stu-id="76378-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76378-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76378-122">-InputObject</span></span>
<span data-ttu-id="76378-123">Obiekt Input</span><span class="sxs-lookup"><span data-stu-id="76378-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76378-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="76378-124">-Name</span></span>
<span data-ttu-id="76378-125">Nazwa konta miejsca do magazynowania, które ma zostać użyte</span><span class="sxs-lookup"><span data-stu-id="76378-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76378-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76378-126">-ResourceGroupName</span></span>
<span data-ttu-id="76378-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="76378-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76378-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76378-128">-ResourceId</span></span>
<span data-ttu-id="76378-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="76378-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76378-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="76378-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="76378-131">Podaj klucz dostępu do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="76378-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76378-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76378-132">-Confirm</span></span>
<span data-ttu-id="76378-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="76378-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76378-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76378-134">-WhatIf</span></span>
<span data-ttu-id="76378-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76378-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76378-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="76378-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76378-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76378-137">CommonParameters</span></span>
<span data-ttu-id="76378-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76378-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76378-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76378-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76378-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76378-140">INPUTS</span></span>

### <span data-ttu-id="76378-141">System.String</span><span class="sxs-lookup"><span data-stu-id="76378-141">System.String</span></span>

### <span data-ttu-id="76378-142">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="76378-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="76378-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76378-143">OUTPUTS</span></span>

### <span data-ttu-id="76378-144">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="76378-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="76378-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76378-145">NOTES</span></span>

## <span data-ttu-id="76378-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76378-146">RELATED LINKS</span></span>
