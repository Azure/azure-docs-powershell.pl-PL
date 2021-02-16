---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4bdf13b485486a8e3c40023ea0011d12b21a93b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238180"
---
# <span data-ttu-id="b6f1b-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6f1b-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="b6f1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f1b-103">Tworzy nowe konto w sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="b6f1b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6f1b-104">SYNTAX</span></span>

### <span data-ttu-id="b6f1b-105">UserOrSystemAssignedEncryption (Default)</span><span class="sxs-lookup"><span data-stu-id="b6f1b-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6f1b-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="b6f1b-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6f1b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6f1b-107">DESCRIPTION</span></span>
<span data-ttu-id="b6f1b-108">Polecenie **cmdlet New-AzDataLakeStoreAccount** tworzy nowe konto data lake store.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="b6f1b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6f1b-109">EXAMPLES</span></span>

### <span data-ttu-id="b6f1b-110">Przykład 1. Tworzenie konta</span><span class="sxs-lookup"><span data-stu-id="b6f1b-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="b6f1b-111">To polecenie tworzy konto usługi Data Lake Store o nazwie ContosoADL dla lokalizacji Wschód USA 2.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="b6f1b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6f1b-112">PARAMETERS</span></span>

### <span data-ttu-id="b6f1b-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="b6f1b-113">-DefaultGroup</span></span>
<span data-ttu-id="b6f1b-114">Określa identyfikator obiektu grupy AzureActive Directory, która ma być domyślnie właścicielem grupy dla nowych plików i folderów.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f1b-115">-DefaultProfile</span></span>
<span data-ttu-id="b6f1b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b6f1b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6f1b-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="b6f1b-117">-DisableEncryption</span></span>
<span data-ttu-id="b6f1b-118">Oznacza, że do konta nie zostanie zastosowana jakakolwiek forma szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f1b-119">— Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="b6f1b-119">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f1b-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b6f1b-120">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f1b-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="b6f1b-121">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f1b-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="b6f1b-122">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f1b-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b6f1b-123">-Location</span></span>
<span data-ttu-id="b6f1b-124">Określa lokalizację do użycia dla konta.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="b6f1b-125">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b6f1b-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b6f1b-126">Wschód STANÓW ZJEDNOCZONYCH 2</span><span class="sxs-lookup"><span data-stu-id="b6f1b-126">East US 2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f1b-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b6f1b-127">-Name</span></span>
<span data-ttu-id="b6f1b-128">Określa nazwę konta do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-128">Specifies the name of the account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f1b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f1b-129">-ResourceGroupName</span></span>
<span data-ttu-id="b6f1b-130">Określa nazwę grupy zasobów zawierającej konto.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-130">Specifies the name of the resource group that contains the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f1b-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="b6f1b-131">-Tag</span></span>
<span data-ttu-id="b6f1b-132">Określa tagi jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="b6f1b-133">Za pomocą tagów możesz zidentyfikować konto usługi Data Lake Store z innych zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f1b-134">- Warstwa</span><span class="sxs-lookup"><span data-stu-id="b6f1b-134">-Tier</span></span>
<span data-ttu-id="b6f1b-135">Żądana warstwa zobowiązania dla tego konta do użycia.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-135">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f1b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f1b-136">CommonParameters</span></span>
<span data-ttu-id="b6f1b-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6f1b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f1b-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f1b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f1b-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6f1b-139">INPUTS</span></span>

### <span data-ttu-id="b6f1b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b6f1b-140">System.String</span></span>

### <span data-ttu-id="b6f1b-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6f1b-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b6f1b-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b6f1b-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b6f1b-143">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="b6f1b-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b6f1b-144">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b6f1b-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b6f1b-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6f1b-145">OUTPUTS</span></span>

### <span data-ttu-id="b6f1b-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6f1b-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="b6f1b-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6f1b-147">NOTES</span></span>

## <span data-ttu-id="b6f1b-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6f1b-148">RELATED LINKS</span></span>

[<span data-ttu-id="b6f1b-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6f1b-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b6f1b-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6f1b-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b6f1b-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6f1b-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="b6f1b-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b6f1b-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


