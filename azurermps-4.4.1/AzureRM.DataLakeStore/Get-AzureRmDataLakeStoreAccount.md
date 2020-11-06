---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c05ca64db5b04ef78778e39d9ae6347db4ca05b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527597"
---
# <span data-ttu-id="a0c82-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a0c82-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="a0c82-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0c82-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c82-103">Pobiera szczegóły konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a0c82-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0c82-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0c82-104">SYNTAX</span></span>

### <span data-ttu-id="a0c82-105">Wszystkie w abonamentach (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a0c82-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c82-106">Cała grupa zasobów</span><span class="sxs-lookup"><span data-stu-id="a0c82-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0c82-107">Określone konto</span><span class="sxs-lookup"><span data-stu-id="a0c82-107">Specific Account</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0c82-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a0c82-108">DESCRIPTION</span></span>
<span data-ttu-id="a0c82-109">Polecenie cmdlet **Get-AzureRmDataLakeStoreAccount** pobiera szczegóły konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a0c82-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="a0c82-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0c82-110">EXAMPLES</span></span>

### <span data-ttu-id="a0c82-111">Przykład 1: Uzyskiwanie konta w usłudze Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="a0c82-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="a0c82-112">To polecenie uzyskuje konto o nazwie ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="a0c82-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="a0c82-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0c82-113">PARAMETERS</span></span>

### <span data-ttu-id="a0c82-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0c82-114">-Name</span></span>
<span data-ttu-id="a0c82-115">Określa nazwę konta, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="a0c82-115">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0c82-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0c82-116">-ResourceGroupName</span></span>
<span data-ttu-id="a0c82-117">Określa nazwę grupy zasobów zawierającej konto usługi Data Lake Store, które ma zostać nadane.</span><span class="sxs-lookup"><span data-stu-id="a0c82-117">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0c82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c82-118">-DefaultProfile</span></span>
<span data-ttu-id="a0c82-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0c82-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0c82-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c82-120">CommonParameters</span></span>
<span data-ttu-id="a0c82-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0c82-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c82-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0c82-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c82-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0c82-123">INPUTS</span></span>

## <span data-ttu-id="a0c82-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0c82-124">OUTPUTS</span></span>

### <span data-ttu-id="a0c82-125">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a0c82-125">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="a0c82-126">Twoje konto usługi Data Lake Store z prośbą o szczegółowe dane.</span><span class="sxs-lookup"><span data-stu-id="a0c82-126">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="a0c82-127">Lista<PSDataLakeStoreAccount></span><span class="sxs-lookup"><span data-stu-id="a0c82-127">List<PSDataLakeStoreAccount></span></span>
<span data-ttu-id="a0c82-128">Lista kont usługi Data Lake Store w określonej grupie zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a0c82-128">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="a0c82-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0c82-129">NOTES</span></span>

## <span data-ttu-id="a0c82-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0c82-130">RELATED LINKS</span></span>

[<span data-ttu-id="a0c82-131">Nowe — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a0c82-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="a0c82-132">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a0c82-132">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="a0c82-133">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a0c82-133">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="a0c82-134">Test — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a0c82-134">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


