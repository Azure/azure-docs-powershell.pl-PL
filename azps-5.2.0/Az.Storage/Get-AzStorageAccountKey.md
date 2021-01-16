---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325080"
---
# <span data-ttu-id="480cd-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="480cd-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="480cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="480cd-102">SYNOPSIS</span></span>
<span data-ttu-id="480cd-103">Pobiera klucze dostępu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="480cd-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="480cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="480cd-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="480cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="480cd-105">DESCRIPTION</span></span>
<span data-ttu-id="480cd-106">Polecenie cmdlet **Get-AzStorageAccountKey** pobiera klucze dostępu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="480cd-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="480cd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="480cd-107">EXAMPLES</span></span>

### <span data-ttu-id="480cd-108">Przykład 1: uzyskiwanie klawiszy dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="480cd-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="480cd-109">To polecenie pobiera klucze określonego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="480cd-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="480cd-110">Przykład 2: uzyskiwanie określonego klucza dostępu dla konta magazynu</span><span class="sxs-lookup"><span data-stu-id="480cd-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="480cd-111">Przykład 3: Lista klawiszy dostępu dla konta magazynu zawiera klucze Kerberos (Jeśli usługa Active Directory jest włączona)</span><span class="sxs-lookup"><span data-stu-id="480cd-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="480cd-112">To polecenie pobiera klucze określonego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="480cd-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="480cd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="480cd-113">PARAMETERS</span></span>

### <span data-ttu-id="480cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480cd-114">-DefaultProfile</span></span>
<span data-ttu-id="480cd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="480cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="480cd-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="480cd-116">-ListKerbKey</span></span>
<span data-ttu-id="480cd-117">Wyświetla listę kluczy Kerberos (Jeśli usługa Active Directory jest włączona) dla określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="480cd-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="480cd-118">Klucz Kerberos jest generowany dla każdego konta magazynu dla uwierzytelniania opartego na tożsamości plików platformy Azure przy użyciu usługi domenowych Active Directory (Azure AD DS) lub usługi domenowych Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="480cd-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="480cd-119">Jest ona używana jako hasło tożsamości zarejestrowanej w usłudze domeny, która reprezentuje konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="480cd-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="480cd-120">Klucz Kerberos nie zapewnia uprawnień dostępu do wykonywania operacji odczytu lub lub zapisu w płaszczyźnie danych na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="480cd-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="480cd-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="480cd-121">-Name</span></span>
<span data-ttu-id="480cd-122">Określa nazwę konta magazynu, dla którego to polecenie cmdlet pobiera klucze.</span><span class="sxs-lookup"><span data-stu-id="480cd-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="480cd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="480cd-123">-ResourceGroupName</span></span>
<span data-ttu-id="480cd-124">Określa nazwę grupy zasobów zawierającej konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="480cd-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="480cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480cd-125">CommonParameters</span></span>
<span data-ttu-id="480cd-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="480cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480cd-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="480cd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480cd-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="480cd-128">INPUTS</span></span>

### <span data-ttu-id="480cd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="480cd-129">System.String</span></span>

## <span data-ttu-id="480cd-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="480cd-130">OUTPUTS</span></span>

### <span data-ttu-id="480cd-131">Microsoft. Azure. Management. Storage. MODELES. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="480cd-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="480cd-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="480cd-132">NOTES</span></span>

## <span data-ttu-id="480cd-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="480cd-133">RELATED LINKS</span></span>

[<span data-ttu-id="480cd-134">Nowe — AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="480cd-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


