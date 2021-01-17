---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 9547a3f3aed86bd7458f9fbf1f1a4375e2d95086
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360866"
---
# <span data-ttu-id="24208-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="24208-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="24208-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24208-102">SYNOPSIS</span></span>
<span data-ttu-id="24208-103">Ustawia poświadczenia konta magazynu dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="24208-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="24208-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24208-104">SYNTAX</span></span>

### <span data-ttu-id="24208-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24208-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24208-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24208-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24208-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24208-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24208-108">Opis</span><span class="sxs-lookup"><span data-stu-id="24208-108">DESCRIPTION</span></span>
<span data-ttu-id="24208-109">Polecenie cmdlet **Set-AzDataBoxEdgeStorageAccountCredential** aktualizuje poświadczenia konta magazynu odpowiadające kontu magazynu na urządzeniu z danymi na krawędziach pola danych.</span><span class="sxs-lookup"><span data-stu-id="24208-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="24208-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24208-110">EXAMPLES</span></span>

### <span data-ttu-id="24208-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24208-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="24208-112">Pomaga w obracaniu klawiszy dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="24208-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="24208-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24208-113">PARAMETERS</span></span>

### <span data-ttu-id="24208-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24208-114">-AsJob</span></span>
<span data-ttu-id="24208-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="24208-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24208-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24208-116">-DefaultProfile</span></span>
<span data-ttu-id="24208-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24208-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24208-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="24208-118">-DeviceName</span></span>
<span data-ttu-id="24208-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="24208-119">Device Name</span></span>

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

### <span data-ttu-id="24208-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="24208-120">-EncryptionKey</span></span>
<span data-ttu-id="24208-121">Klucz szyfrowania urządzenia brzegowego</span><span class="sxs-lookup"><span data-stu-id="24208-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="24208-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="24208-122">-InputObject</span></span>
<span data-ttu-id="24208-123">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="24208-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24208-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24208-124">-Name</span></span>
<span data-ttu-id="24208-125">Nazwa konta magazynu, które ma być używane</span><span class="sxs-lookup"><span data-stu-id="24208-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24208-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24208-126">-ResourceGroupName</span></span>
<span data-ttu-id="24208-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="24208-127">Resource Group Name</span></span>

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

### <span data-ttu-id="24208-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24208-128">-ResourceId</span></span>
<span data-ttu-id="24208-129">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="24208-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="24208-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="24208-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="24208-131">Podaj klucz dostępu do konta magazynu</span><span class="sxs-lookup"><span data-stu-id="24208-131">provide storage account access key</span></span>

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

### <span data-ttu-id="24208-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24208-132">-Confirm</span></span>
<span data-ttu-id="24208-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24208-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24208-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24208-134">-WhatIf</span></span>
<span data-ttu-id="24208-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24208-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24208-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24208-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24208-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24208-137">CommonParameters</span></span>
<span data-ttu-id="24208-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24208-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24208-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24208-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24208-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24208-140">INPUTS</span></span>

### <span data-ttu-id="24208-141">System. String</span><span class="sxs-lookup"><span data-stu-id="24208-141">System.String</span></span>

### <span data-ttu-id="24208-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="24208-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="24208-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24208-143">OUTPUTS</span></span>

### <span data-ttu-id="24208-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="24208-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="24208-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24208-145">NOTES</span></span>

## <span data-ttu-id="24208-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24208-146">RELATED LINKS</span></span>
