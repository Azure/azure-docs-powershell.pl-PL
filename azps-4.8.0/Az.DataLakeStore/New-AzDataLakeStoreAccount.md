---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4bdf13b485486a8e3c40023ea0011d12b21a93b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221281"
---
# <span data-ttu-id="18edc-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="18edc-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="18edc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18edc-102">SYNOPSIS</span></span>
<span data-ttu-id="18edc-103">Tworzy nowe konto w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="18edc-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="18edc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18edc-104">SYNTAX</span></span>

### <span data-ttu-id="18edc-105">UserOrSystemAssignedEncryption (domyślny)</span><span class="sxs-lookup"><span data-stu-id="18edc-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18edc-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="18edc-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18edc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="18edc-107">DESCRIPTION</span></span>
<span data-ttu-id="18edc-108">Polecenie cmdlet **New-AzDataLakeStoreAccount** tworzy nowe konto usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="18edc-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="18edc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18edc-109">EXAMPLES</span></span>

### <span data-ttu-id="18edc-110">Przykład 1. Tworzenie konta</span><span class="sxs-lookup"><span data-stu-id="18edc-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="18edc-111">To polecenie tworzy konto usługi Data Lake Store o nazwie ContosoADL dla pozycji wschód w Stanach Zjednoczonych 2.</span><span class="sxs-lookup"><span data-stu-id="18edc-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="18edc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18edc-112">PARAMETERS</span></span>

### <span data-ttu-id="18edc-113">-Domyślna</span><span class="sxs-lookup"><span data-stu-id="18edc-113">-DefaultGroup</span></span>
<span data-ttu-id="18edc-114">Określa identyfikator obiektu katalogu AzureActive, który ma być używany jako domyślny właściciel grupy dla nowych plików i folderów.</span><span class="sxs-lookup"><span data-stu-id="18edc-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="18edc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18edc-115">-DefaultProfile</span></span>
<span data-ttu-id="18edc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="18edc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18edc-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="18edc-117">-DisableEncryption</span></span>
<span data-ttu-id="18edc-118">Wskazuje, że do konta nie zastosowano żadnej formy szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="18edc-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

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

### <span data-ttu-id="18edc-119">— Szyfrowanie</span><span class="sxs-lookup"><span data-stu-id="18edc-119">-Encryption</span></span>
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

### <span data-ttu-id="18edc-120">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="18edc-120">-KeyName</span></span>
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

### <span data-ttu-id="18edc-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="18edc-121">-KeyVaultId</span></span>
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

### <span data-ttu-id="18edc-122">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="18edc-122">-KeyVersion</span></span>
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

### <span data-ttu-id="18edc-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="18edc-123">-Location</span></span>
<span data-ttu-id="18edc-124">Określa lokalizację, w której ma być używane konto.</span><span class="sxs-lookup"><span data-stu-id="18edc-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="18edc-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="18edc-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18edc-126">Wschód USA 2</span><span class="sxs-lookup"><span data-stu-id="18edc-126">East US 2</span></span>

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

### <span data-ttu-id="18edc-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="18edc-127">-Name</span></span>
<span data-ttu-id="18edc-128">Określa nazwę konta, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="18edc-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="18edc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18edc-129">-ResourceGroupName</span></span>
<span data-ttu-id="18edc-130">Określa nazwę grupy zasobów zawierającej dane konto.</span><span class="sxs-lookup"><span data-stu-id="18edc-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="18edc-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="18edc-131">-Tag</span></span>
<span data-ttu-id="18edc-132">Określa znaczniki jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="18edc-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="18edc-133">Za pomocą znaczników możesz identyfikować konta usługi Data Lake Store z innych zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="18edc-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="18edc-134">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="18edc-134">-Tier</span></span>
<span data-ttu-id="18edc-135">Pożądana warstwa zobowiązań do użycia dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="18edc-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="18edc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18edc-136">CommonParameters</span></span>
<span data-ttu-id="18edc-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18edc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18edc-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18edc-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18edc-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18edc-139">INPUTS</span></span>

### <span data-ttu-id="18edc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="18edc-140">System.String</span></span>

### <span data-ttu-id="18edc-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="18edc-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="18edc-142">System. Nullable "1 [[Microsoft. Azure. Management. datalake. Store. MODELES. EncryptionConfigType, Microsoft. Azure. Management. datalake. Store, wersja = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="18edc-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="18edc-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18edc-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="18edc-144">System. Nullable "1 [[Microsoft. Azure. Management. datalake. Store......... usługi. Microsoft. Azure. Management. datalake. Store.</span><span class="sxs-lookup"><span data-stu-id="18edc-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="18edc-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18edc-145">OUTPUTS</span></span>

### <span data-ttu-id="18edc-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="18edc-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="18edc-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18edc-147">NOTES</span></span>

## <span data-ttu-id="18edc-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18edc-148">RELATED LINKS</span></span>

[<span data-ttu-id="18edc-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="18edc-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="18edc-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="18edc-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="18edc-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="18edc-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="18edc-152">Test — AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="18edc-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


